# # Healthcare Claims Data Analysis
### Assignment – Claims HEADER, LINE, and CODE Files

## Project Description
This project analyzes a sample of prospective healthcare claims from Stony Brook University Hospital. The goal is to examine patterns in billing activity, diagnosis codes, procedure codes, payer distribution, and place of service using three related datasets. All analysis was performed in Python using pandas for data manipulation and matplotlib for basic visualizations all in a jupyter notebook.

The notebook demonstrates how to:
- Load and explore relational claims datasets
- Merge the HEADER, LINE, and CODE files into combined tables
- Calculate summary metrics used in healthcare data and revenue cycle analysis
- Create simple charts to support interpretation of the results

---

## Data Source Information
This project uses three CSV files that are linked by a shared claim identifier :

| File Name                     | Description                                                                 |
|-------------------------------|-----------------------------------------------------------------------------|
| STONYBRK_20240531_HEADER.csv  | One row per claim; includes payer, provider, dates of service, and POS     |
| STONYBRK_20240531_LINE.csv    | One row per billed service line; includes HCPCS/CPT, modifiers, units, charges |
| STONYBRK_20240531_CODE.csv    | One row per ICD-10 diagnosis code associated with each claim               |


---

## How to Run the Notebook

1. Install Python.
2. Install the required Python libraries by running:

   pip install -r requirements.txt

3. Make sure your project folder is organized as follows:

   claims-analysis/
     data/
       STONYBRK_20240531_HEADER.csv
       STONYBRK_20240531_LINE.csv
       STONYBRK_20240531_CODE.csv
     notebooks/
       claims_analysis.ipynb
     README.md
     requirements.txt

4. Open the notebook with:

   jupyter notebook notebooks/claims_analysis.ipynb

5. Run all cells in order from top to bottom.

---

## Summary of Key Findings

- A small number of provider groups are responsible for most of the claims, showing that billing volume is concentrated among high-activity practices.
- Medicare is the dominant primary payer in this dataset, while Medicaid and commercial payers account for a smaller share of claims.
- The most frequent diagnosis codes include respiratory failure, hypertension, heart disease, and serious neurological conditions, indicating a largely high-acuity patient population.
- Commonly billed procedure codes include critical care (99291) and inpatient evaluation and management services, which are consistent with the serious diagnoses observed.
- Most claims originate in inpatient hospital settings, with fewer claims coming from office, outpatient hospital, or emergency department locations.

---

## Required Libraries
The analysis notebook uses the following Python libraries:

- pandas (version 1.3.0 or higher)
- matplotlib (version 3.4.0 or higher)
- seaborn (version 0.11.0 or higher)
