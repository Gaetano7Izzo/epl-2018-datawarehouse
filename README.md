# 🏆 Premier League 2018-19 Data Warehouse & Analytics

[![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![GitHub License](https://img.shields.io/github/license/Gaetano7Izzo/epl-2018-datawarehouse)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

**Analisi avanzata del campionato inglese** con modellazione DWH a fiocco di neve e visualizzazioni interattive.

---

## 📌 Struttura del Progetto

```bash
epl-2018-datawarehouse/
├── data/
│   ├── raw/          # Dati originali da FootyStats.org
│   └── processed/    # Dataset puliti (matches, players, teams)
├── documentation/    # Tesina PDF e diagrammi tecnici
├── models/           # Modelli ER e DWH (immagini)
├── powerbi/          # File .pbix completo
└── analysis_screenshots/  # Grafici esportati
```

🔥 Key Insights 
⚽ Performance Squadre
Top 3 marcatori: Salah, Aubameyang, Mané (22 goal)
https://analysis_screenshots/top_scorers.png

Goal in casa: Heatmap per giornata (Arsenal leader con 40 goal)

sql
-- Esempio query
SELECT home_team, SUM(home_goals) 
FROM matches 
WHERE season = '2018-2019' 
GROUP BY home_team
ORDER BY 2 DESC

📊 Dettaglio Arbitri
Arbitri più attivi: Anthony Taylor, Michael Oliver
https://analysis_screenshots/referee_analysis.png

🏟️ Affluenza
Record spettatori: Man Utd (74k/media) vs Huddersfield (24k/media)
https://analysis_screenshots/attendance.png

🛠 Come Ricostruire il Progetto
Requisiti:

- Power BI Desktop (versione 2023+)
- Accesso a FootyStats.org (opzionale)

Passaggi
Clona la repo:

bash
git clone https://github.com/Gaetano7Izzo/epl-2018-datawarehouse.git
Apri il file Power BI:

Modifica i percorsi delle sorgenti dati in powerbi/premier_league.pbix

Esplora i dati:

Usa i dataset in data/processed/ per analisi personalizzate

📄 Licenza
Creative Commons BY-NC-SA 4.0 - Utilizzo non commerciale con attribuzione

Autori: Gaetano Emanuele Izzo, Eugenio Iandoli, Aniello Gaudino
Ultimo aggiornamento: Agosto 2023
