# Global Food Security Analytics (2001-2023) 🌍🌾

## Obiettivo del Progetto
Questo progetto analizza l'evoluzione della sicurezza alimentare globale nell'arco di oltre vent'anni, incrociando fattori macroeconomici (PIL, Inflazione), agricoli (Uso del suolo, Resa dei cereali) e sociali (Accesso all'acqua e igiene). L'obiettivo è fornire un cruscotto interattivo per identificare i "pain points" strutturali che portano i paesi verso crisi alimentari croniche.

## Architettura Tecnica & Scelte di Design
Questo progetto è stato sviluppato con un approccio ibrido (Back-end + Front-end):

1. **Back-end Data Modeling (SQL):** Nella cartella `sql_scripts/` è presente la struttura di pre-aggregazione. Sono state sviluppate 12 View complesse per gestire calcoli storici, ranking e variazioni YoY, utili qualora il reporting avvenga tramite tool di visualizzazione web-based.
2. **Front-end & Visual Analytics (Power BI):** Per massimizzare le performance del motore VertiPaq e permettere l'esplorazione dinamica dei dati, il report in Power BI utilizza un Modello a Stella (Star Schema) partendo dalla tabella dei fatti grezza.
3. **Misure DAX Avanzate:** Tutte le metriche di business (incluse le variazioni pre/post pandemia COVID-19) sono state ricreate in DAX per reagire istantaneamente al "Filter Context".
4. **UX & Navigazione:** Implementazione di "Parametri Campo" (Field Parameters) per grafici dinamici e azioni di "Drill-through" per analisi verticali sui singoli paesi.

## Struttura della Dashboard (5 Pagine)
* **Page 1 - Executive Overview:** Mappa coropletica e KPI globali.
* **Page 2 - Dinamiche Macroeconomiche:** Analisi bivariata PIL vs Fame e impatto COVID-19.
* **Page 3 - Resilienza Agricola:** Dipendenza dalle importazioni commerciali e stress idrico.
* **Page 4 - Country Drill-down:** Scheda tecnica dinamica per l'analisi storica di una singola nazione.
* **Page 5 - Fattori Sociali:** Analisi delle infrastrutture di base (Acqua e Igiene) tramite selettori dinamici delle metriche.
