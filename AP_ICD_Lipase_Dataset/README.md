# AP_ICD_Lipase_Dataset.ipynb

**Description:** This notebook filters patients who have undergone lipase tests and diagnoses them with Acute Pancreatitis (AP) using the associated ICD code.

**Difference:** Compared to the AP_ICD_Dataset, this includes an additional feature, `lipase_level`.

# AP_ICD_Lipase_Dataset.csv

**Description:** This dataset includes all unique patients who have had lipase tests and are diagnosed with AP, filtered by their `subject_id`. The selection criteria are:
- If a patient has multiple records, only one record is considered. If the patient is deceased, any record can be used; otherwise, the record with the longest length of stay is selected.

**Usage:**
- Predict the length of stay for patients diagnosed with AP.
- Develop a new feature based on length of stay to classify AP into categories (mild, severe, or extreme) for multi-label classification.
- Support the development of a GUI to predict the length of stay (L.O.S).

# AP_ICD_Lipase_Comorbidities_Dataset.csv

**Description:** Derived from the `AP_ICD_Lipase_Dataset.csv`, this dataset includes additional diagnosis details, listing all other diseases identified in the same patients to analyze correlations between AP and other potentially fatal conditions (leading to increased length of stay or death).

**Usage:**
- Examine which comorbidities, when present with AP, may increase the risk of fatal outcomes in patients.

