# AP_ICD_LP_Filter_Dataset.ipynb

**Description:** This notebook filters patients whose lipase levels are greater than or equal to three times the normal levels and are diagnosed with Acute Pancreatitis (AP) using the related ICD code.

# High_Lipase_Dataset.csv

**Description:** This dataset includes all unique patients with elevated lipase levels, filtered by their `subject_id`. It uses the following criteria for selection:
- If a patient has multiple records, only one record is considered. If the patient is deceased, any record can be used; otherwise, the record with the longest length of stay is selected.

# High_Lipase_Comorbidities_Dataset.csv

**Description:** Derived from the `High_Lipase_Dataset.csv`, this dataset includes additional diagnosis details, listing all other diseases identified in the same patients to analyze broader health patterns.

# High_LP_AP_ICD_Dataset.csv

**Description:** This dataset comprises all unique patients with elevated lipase levels who are also diagnosed with AP, filtered by their `subject_id`. The selection criteria are:
- If a patient has multiple records, only one record is considered. If the patient is deceased, any record can be used; otherwise, the record with the longest length of stay is selected.

# High_LP_AP_ICD_Comorbidities_Dataset.csv

**Description:** Built on the `High_LP_AP_ICD_Dataset.csv`, this dataset includes further diagnoses, identifying additional diseases in the same patients to explore correlations between AP and other potentially fatal conditions (leading to increased length of stay or death).

