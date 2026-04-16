# Global Food Security Analytics (2001-2023) 🌍🌾

## 🎯 Obiettivo del Progetto
Questo progetto nasce per analizzare l'evoluzione della sicurezza alimentare globale nell'arco di un ventennio. L'obiettivo è trasformare dati grezzi in insight strategici, identificando le correlazioni tra ricchezza economica, efficienza agricola e infrastrutture sociali per comprendere le cause profonde delle crisi alimentari croniche.

## 🛠️ Architettura Tecnica e Scelte Progettuali
Il progetto segue un approccio **End-to-End Data Lifecycle**:

1.  **Data Cleaning (Python):** Normalizzazione dei nomi geografici (es. Egitto, Turchia) per garantire una geocodifica accurata al 100% su Bing Maps.
2.  **Back-end Modeling (SQL):** Creazione di 12 View complesse per gestire aggregazioni storiche e ranking. Sebbene il report finale usi il motore DAX, queste View dimostrano la capacità di strutturare un data warehouse scalabile.
3.  **Front-end Analytics (Power BI):** Implementazione di uno **Star Schema** (Schema a Stella) con tabelle Dimensioni (`DimPaesi`, `DimAnni`) e Fatti, ottimizzando le performance di calcolo.
4.  **Advanced DAX:** Sviluppo di misure dinamiche per il calcolo di variazioni Year-over-Year (YoY) e l'impatto di shock globali (COVID-19).

---

## 📊 Analisi Dettagliata delle Dashboard

### Pagina 1: Executive Overview (Il Polso Globale)
* **Mappa:** Visualizza l'intensità della fame nel mondo. Permette di identificare istantaneamente le aree critiche (Africa Sub-Sahariana e Sud Asia) e monitorare la diffusione geografica dell'insicurezza alimentare.
* **KPI Cards (Indice Fame e Variazione YoY):** Forniscono una metrica immediata della tendenza globale. La variazione percentuale anno su anno serve a capire se la crisi sta accelerando o rientrando.
* **Contatore Paesi in Crisi:** Quantifica quante nazioni superano la soglia di allerta, offrendo un indicatore di volume sulla gravità del periodo selezionato.

### Pagina 2: Macroeconomia e Shock Esterni
* **Scatter Chart (PIL vs Indice Fame):** Analizza il legame tra potenza economica e fame. Identifica gli "outlier": paesi che pur avendo un PIL in crescita non riescono a ridurre la denutrizione, evidenziando problemi di distribuzione interna.
* **Analisi Impatto COVID-19:** Un confronto visivo tra il periodo pre e post 2020 per misurare quanto la pandemia abbia eroso anni di progressi nella sicurezza alimentare.

### Pagina 3: Resilienza Agricola e Commercio
* **Dipendenza dalle Importazioni:** Mette a confronto la produzione interna con il cibo importato. Un'alta dipendenza indica vulnerabilità alle fluttuazioni dei prezzi dei mercati internazionali.
* **Evoluzione Uso del Suolo:** Analizza se l'aumento della produzione è dovuto a una reale efficienza tecnologica (resa) o a un'espansione insostenibile delle terre arabili (deforestazione).

### Pagina 4: Country Drill-down (Analisi Verticale)
* **Trend Storico Lineare:** Permette di studiare il percorso di una singola nazione. Utile per capire se una crisi è un evento isolato o un trend decadente.
* **Timeline delle Crisi (Flag Emergente):** Una "striscia di allarme" rossa che evidenzia la frequenza degli stati di emergenza, permettendo di distinguere tra shock temporanei e fragilità strutturali croniche.
* **Confronto Produzione vs Resa:** Analizza se il settore agricolo locale sta migliorando grazie all'innovazione (più kg per ettaro) o solo aumentando i volumi.

### Pagina 5: Driver Sociali e Infrastrutture
* **Grafico Dinamico (Field Parameters):** Un selettore avanzato che permette all'utente di scambiare le metriche sull'asse Y (es. Mortalità Infantile vs PIL). Dimostra come la carenza di servizi di base influenzi direttamente la salute pubblica.
* **Accesso ad Acqua e Igiene per Regione:** Analizza le cause "invisibili". Mostra come la mancanza di infrastrutture igieniche sia spesso un moltiplicatore della malnutrizione, indipendentemente dalla quantità di cibo disponibile.
 Una tabella che classifica i paesi in base alla percentuale di anni trascorsi in stato di crisi, identificando dove gli aiuti internazionali hanno avuto meno impatto.

---

