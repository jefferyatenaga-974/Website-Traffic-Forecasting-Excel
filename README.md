# Website Traffic Forecasting (Excel)

A data pipeline and forecasting project using Excel, predicting near-future website traffic from real historical visitor data, with a weekday-adjusted forecast that outperforms a plain trend line.

## Tools Used
- Microsoft Excel (WPS Office Spreadsheets)
- Built-in FORECAST function, AVERAGEIF

## Dataset
[Daily Website Visitors](https://www.kaggle.com/datasets/bobnau/daily-website-visitors) — real daily traffic data from an academic forecasting course website (statforecasting.com), September 2014 to August 2020 (~2,167 rows).

## What This Project Does
1. Cleans and validates the raw data (fixes text-formatted dates, checks for duplicates, removes a stray row)
2. Builds a basic trend forecast using Excel's FORECAST function
3. Identifies that the basic forecast misses a real weekly pattern (busy Thursdays, quiet Saturdays)
4. Builds a weekday-adjusted forecast that corrects for this pattern
5. Visualizes the last 14 real days next to the 3 forecasted days in one chart

## Key Findings
- **Basic trend forecast:** nearly flat, ~4,256 page loads predicted for all 3 future days, missing real weekly variation
- **Weekday-adjusted forecast:** Thursday 4,790.54, Friday 3,859.17, Saturday 2,640.46, correctly reflecting the real weekly pattern in the data
- **Real weekday averages found in the data:** Thursday ~4,651 page loads, Saturday ~2,501 page loads

## Data Pipeline / Cleaning Steps
1. Converted the Date column from text to real dates (Split Text to Columns trick)
2. Checked for duplicate rows using Remove Duplicates (none found)
3. Removed a stray, incomplete row introduced during formula testing

## Files in This Repo
- `Website_Traffic_Forecast_Writeup.pdf` — full write-up with methodology, results, and recommendations
- `notes/project_notes.md` — process notes and roadblocks encountered

## Full Write-Up
See `Website_Traffic_Forecast_Writeup.pdf` for the complete write-up, including the forecast comparison table and business recommendations.
