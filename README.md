# GoogleStockData
## SQL DB Creation

### Alphabet Inc. (Google) Comprehensive SQL Database
Ho trasformato un dataset grezzo (CSV) in un database relazionale strutturato su MariaDB/MySQL, ripulendo i dati e organizzandoli in 6 tabelle correlate per analisi finanziarie e di mercato.

### Data Engineering & Cleaning
- Normalizzazione: Suddivisione dei dati in tabelle specifiche per ridurre la ridondanza.
- Data Typing: Impostazione di formati precisi (Decimal per i valori monetari, Date per le serie storiche, Int per i volumi).
- Integrità: Strutturazione dei dati per supportare analisi di serie temporali (Daily Prices) e confronti tra segmenti di ricavo.

### Architettura del Database
Il database Google_Stock_Data è composto da:
Tabella	Descrizione
- annual_financials	Metriche annuali (Revenue, Net Income, EPS) dal 2004 al 2026.
- company_info	Milestone aziendali, acquisizioni e info sulle classi di azioni.
- financial_ratios	Indicatori di performance (P/E Ratio, ecc.) per analisi fondamentale.
- quarterly_earnings	Risultati trimestrali per analisi di stagionalità.
- revenue_segments	Suddivisione dei ricavi per rami d'azienda (Cloud, Ads, ecc.).
- stock_daily_prices	Storico giornaliero dei prezzi di borsa (Apertura, Chiusura, Volumi).

### Esempio di Analisi Avanzata
Con questa struttura è possibile eseguire query complesse, come il calcolo del Profit Margin annuale:

SELECT Year, (Net_Income_Billions / Revenue_Billions) * 100 AS Profit_Margin_Percent

FROM annual_financials

WHERE Revenue_Billions > 0;


# ENGLISH VERSION


# GoogleStockData
## SQL DB Creation

### Alphabet Inc. (Google) – Comprehensive SQL Database
I transformed a raw CSV dataset into a structured relational database using MariaDB/MySQL, cleaning the data and organizing it into 6 interconnected tables designed for financial and market analysis.

### Data Engineering & Cleaning
- Normalization: Splitting the dataset into dedicated tables to reduce redundancy.
- Data Typing: Assigning precise formats (Decimal for monetary values, Date for time series, Int for volumes).
- Integrity: Structuring the data to support time‑series analysis (Daily Prices) and comparisons across revenue segments.
 
### Database Architecture
The Google_Stock_Data database consists of the following tables:

- annual_financials: Annual metrics (Revenue, Net Income, EPS) from 2004 to 2026.
- company_info: Company milestones, acquisitions, and information about stock classes.
- financial_ratios: Performance indicators (P/E Ratio, etc.) for fundamental analysis.
- quarterly_earnings: Quarterly results for seasonality analysis.
- revenue_segments: Revenue breakdown by business segments (Cloud, Ads, etc.).
- stock_daily_prices: Daily stock price history (Open, Close, Volume).



### Example of Advanced Analysis
With this structure, it is possible to run complex queries, such as calculating the annual Profit Margin:

SELECT Year, (Net_Income_Billions / Revenue_Billions) * 100 AS Profit_Margin_Percent

FROM annual_financials

WHERE Revenue_Billions > 0;




