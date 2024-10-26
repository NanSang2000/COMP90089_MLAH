# NOT_AP_ICD_Dataset.ipynb

**Description:** This notebook filters out patients who are not diagnosed with Acute Pancreatitis (AP), using the ICD codes specifically for AP, and randomly selects 1500 patients from this group.

# NON_AP_ICD_Dataset.csv

**Description:** This dataset includes all randomly selected unique patients diagnosed with diseases other than AP.

**Usage:**
- Predict the length of stay for patients not diagnosed with AP.
- Combine this dataset with the AP_ICD_Dataset for binary classification to determine the presence of AP.
- Support the development of a GUI to classify whether a patient has AP.

# NON_AP_ICD_Comorbidities_Dataset.csv

**Description:** Derived from the `NON_AP_ICD_Dataset.csv`, this dataset includes additional diagnoses, listing all other diseases identified in the same patients, to explore broader health patterns.

