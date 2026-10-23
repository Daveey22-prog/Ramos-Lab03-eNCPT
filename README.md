# Lab 3 — Standardized Clinical Charting (eNCPT)

## Project
NutriChart: a browser-based clinical charting demonstration organized around the four steps of the Nutrition Care Process.

## Features
- Assessment with food history, patient data, and automatic BMI calculation
- Nutrition diagnosis with structured Problem–Etiology–Signs/Symptoms (PES) statement
- Nutrition intervention with planned action, measurable goals, and follow-up date
- Monitoring/evaluation with indicators, baseline, target, progress, and outcome
- Generated clinical notes, JSON export, TXT export, and print/save as PDF
- Sample fictional patient for demonstration
- All content remains in browser memory until downloaded; no database or backend

## Running the project
1. Extract the ZIP file.
2. Open `index.html` in Chrome or Edge. No installation needed.
3. Select **Load Sample Case** to populate a fictional example.
4. Click each workflow step, examine the form, and finish on **Clinical Note**.
5. Click **Export JSON** and check its structure against `chart.schema.json`.
6. Click **Print / Save PDF** to save the generated note.

Optional local server from this directory: `python -m http.server 8000`, then visit http://localhost:8000

## Files
- `index.html` — working web app
- `chart.schema.json` — JSON Schema for the structured chart
- `sample-chart.json` — matching sample data for Postman testing
- `README.md` — instructions

## Postman workflow (optional)
Postman can validate/inspect the downloaded JSON. For a quick local mock endpoint, create a POST request to a mock server with body set to the contents of `sample-chart.json`. This demo does **not** implement an HTTP API or database; exporting JSON is a client-side action. For local schema validation, use a JSON Schema validator supporting draft 2020-12.

## Scope and terminology disclaimer
The structure follows the four-step Nutrition Care Process. Category labels and selectable example diagnosis phrases are provided for **educational illustration** and are not claimed to be an exhaustive, licensed, or validated eNCPT terminology dataset. eNCPT/NCPT terminology is owned by the Academy of Nutrition and Dietetics and licensed access may be required for official terms/codes. Replace sample terms with authorized, verified entries if your professor requires exact codes. Do not enter real protected health information. This is **not** a medical record system or clinical decision-support tool.

Reference: https://www.eatrightpro.org/practice/nutrition-care-process/ncp-overview
