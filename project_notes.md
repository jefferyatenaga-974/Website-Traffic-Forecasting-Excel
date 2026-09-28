# Project Notes

## Process
- Downloaded the Daily Website Visitors dataset and opened it in Excel (WPS Office Spreadsheets), after Excel 2007 desktop and Excel Online both turned out to lack the features needed for this project.
- Cleaned the data: fixed the Date column (was stored as text), checked for duplicates, removed a stray row introduced while testing formulas.
- Built a basic trend forecast with the FORECAST function, then noticed it produced a nearly flat prediction that ignored the real weekly traffic pattern.
- Calculated weekday averages and a seasonal adjustment, then combined that with the trend forecast to get a more realistic, weekday-adjusted forecast.
- Built a line chart combining the last 14 real days with the 3 forecasted days to visualize the result.

## Roadblocks and How They Were Handled
- **Tool limitations:** Excel 2007 (desktop) lacked Power Query and Forecast Sheet entirely. Excel Online lacked the FORECAST.ETS function. Switched to WPS Office Spreadsheets, a free Excel alternative, and used the classic FORECAST function (linear trend) instead of FORECAST.ETS.
- **Date formatting:** the Date column initially loaded as plain text, which would have broken any date-based analysis. Fixed using Split Text to Columns to force real date recognition.
- **Broken online chart template:** an online chart gallery template overwrote real data with placeholder values. Caught by comparing the chart's data against the source cells, and fixed by rebuilding the data range and formulas.
- **Flat forecast:** the basic FORECAST function alone gave a nearly identical prediction for every future day, missing the real weekly pattern in the data. Fixed by adding a weekday-based seasonal adjustment calculated from the data itself.

## Key Takeaway
A basic forecasting formula is only a starting point. Comparing its output against the real patterns in the data, and adjusting for what it misses, is what turns a technically-correct forecast into a genuinely useful one.
