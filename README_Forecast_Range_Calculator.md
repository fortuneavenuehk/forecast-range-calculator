# Forecast Range Calculator v3

## Purpose
A lightweight browser tool for Sales Operations to turn pipeline data into Low, Call, and High forecast scenarios.

## How to Use
1. Open `forecast_range_calculator_v3.html` in a browser.
2. Upload a pipeline CSV.
3. Confirm the forecast-category and amount columns.
4. Select **Extract Commit / Upside / Pipeline**.
5. Review the extracted deals and totals.
6. Adjust the conversion rates and other forecast inputs as needed.
7. Review the Low, Call, and High scenarios.

## Forecast Logic
- **Low:** Closed Won + Portal Orders + converted Commit
- **Call:** Low + converted Upside + converted Pipeline
- **High:** Call + converted Mega Deal

## CSV Requirements
The CSV should contain:
- A deal or opportunity name column
- A forecast-category column
- An amount column

Recognized categories include:
- Commit
- Upside
- Best Case, mapped to Upside
- Pipeline

The tool allows the user to select the relevant columns if they are not detected automatically.

## Privacy
CSV data is processed locally in the browser. The tool does not upload or store the pipeline file.

## Known Limits
- CSV layouts may require manual column selection.
- Unrecognized forecast categories are ignored.
- Closed Won and Portal Orders are entered manually.
- Conversion rates are user-defined and are not validated against company policy.
- The tool does not connect directly to SFDC or Clari.
- It does not save scenarios or create an audit history.
- Currency display is limited to USD.

## Deliberately Not Fixing in This Version
- Direct SFDC or Clari integration
- User authentication
- Historical forecast tracking
- Multi-currency support
- Forecast commentary generation

## Good-Enough Decision
This version is ready to share because a Sales Operations user can upload pipeline data, validate the extracted deals, adjust assumptions, and generate forecast scenarios without assistance.
