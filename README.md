#📊 Serie A 2015/2016: Approfondimento Analitico con Python e Power BI

## 🎯 Obiettivi del Progetto
L’obiettivo generale del progetto è la realizzazione di uno strumento interattivo, basato su Power BI, in grado di rispondere a domande analitiche come:
1) Come si differenziano le squadre tra loro?
2) Quali sono le principali caratteristiche di squadre e giocatori?
3) Chi ha prodotto di più in termini di rendimento?
4) Chi ha giocato di più?
Un focus particolare è stato dedicato all'analisi della AS Roma, con l'obiettivo specifico di confrontare il rendimento della squadra sotto la guida dei due allenatori della stagione 2015/2016: Rudi Garcia e Luciano Spalletti, entrambi con 19 partite all’attivo.

## 📁 Struttura del Repository
All'interno della cartella CapstoneProject si trovano i due file principali:
1) .ipynb: Notebook Jupyter con l'analisi esplorativa dei dati (EDA) e la costruzione delle tabelle origine per Power BI.
2) .pbix: Il report interattivo completo sviluppato in Power BI.

## 🔍 Origine dei Dati
I dati utilizzati provengono dal repository open source di StatsBomb Open Data.
In particolare, è stata selezionata la stagione 2015/2016 della Serie A, l'ultima disponibile per questo campionato nel dataset.
Ogni partita è identificata da un codice univoco e descritta tramite una tabella di eventi dettagliata. Ogni evento (passaggio, tiro, gol, fallo, sostituzione, ecc.) rappresenta una riga: in media 3500 righe per partita, per un totale di circa 380 partite.

## 🧠 Fase di Analisi Esplorativa (EDA)
L’esplorazione iniziale dei dati è stata condotta in Python, utilizzando principalmente la libreria Pandas.
### Analisi iniziale sulla AS Roma
Per comprendere la struttura del dataset e familiarizzare con le sue colonne, è stato avviato uno studio approfondito su tutte le 38 partite della AS Roma, salvate nella cartella AsRoma_Matches con un file .ipynb dedicato per ogni gara. In questi notebook sono state generate visualizzazioni tramite Matplotlib e Mplsoccer, tra cui:
1) Heatmap dei passaggi
2) Posizione media dei giocatori
3) Rete di passaggi più utilizzata
4) Distribuzione dei tiri e dei gol
Questa fase ha permesso di conoscere la granularità e le potenzialità dei dati, gettando le basi per la costruzione del modello Power BI.

## 🏗️ Costruzione del Modello per Power BI
Una volta analizzata la struttura dei dati, è stato sviluppato in Python un processo di estrazione, trasformazione e selezione delle informazioni più rilevanti, con l'obiettivo di creare un modello dati pulito ed efficiente per Power BI.
### Tabelle create:
Tabelle Dimensionali:
1) DimCoaches
2) DimTeams
3) DimMatches
4) DimPlayers
Tabelle Fatti:
1) FactGoals
2) FactPlayers
3) FactTeams
Queste tabelle sono state salvate in formato .csv per essere caricate in Power BI.
Inoltre, è incluso un file .json creato manualmente per la personalizzazione del tema grafico del report.

## 📊 Il Report Power BI
Il report Power BI (.pbix) è composto da diverse pagine tematiche:
1) Panoramica Generale: statistiche principali del campionato con classifiche per squadre e giocatori
2) Squadra vs Squadra: confronto 1-vs-1 tra due squadre selezionabili
3) Giocatore Singolo: pagina dedicata alle statistiche dettagliate di un giocatore
Focus AS Roma: pagina dedicata alla stagione della Roma, con analisi e grafici derivati dal lavoro in Python (replicati in Power BI), compreso il confronto tra Garcia e Spalletti

## ⚙️ Tecnologie Utilizzate
1) Python (Pandas, Matplotlib, Mplsoccer)
2) Jupyter Notebook
3) Power BI

## 📌 Conclusioni
Questo progetto dimostra come, a partire da un dataset ad alta granularità come quello di StatsBomb, sia possibile estrarre conoscenza, creare insight visivi e costruire uno strumento interattivo e informativo per analizzare un’intera stagione calcistica.
Il workflow adottato valorizza l’unione tra analisi in Python e visualizzazione avanzata in Power BI.
