# AP_ICD_Dataset.ipynb

**Description:** This notebook includes code to filter patients diagnosed with Acute Pancreatitis (AP) solely using the ICD codes for Acute Pancreatitis.

# AP_ICD_Dataset.csv

**Description:** This dataset contains all unique patients diagnosed with AP, filtered by their `subject_id`. It applies the following filtering criteria:
- If a patient has multiple records, only one record is considered. If the patient is deceased, any record can be used; otherwise, the record with the longest length of stay is selected.

**Usage:**
- Predict the length of stay for patients diagnosed with AP.
- Develop a new feature based on length of stay to classify AP into categories (mild, severe, or extreme) for multi-label classification.
- Support the development of a GUI to predict the length of stay (L.O.S).

# AP_ICD_Comorbidities_Dataset.csv

**Description:** This dataset is derived from the `AP_ICD_Dataset.csv` but includes additional diagnosis information for other diseases identified in the same patients, to analyze patterns between AP and other potentially fatal diseases (leading to increased length of stay or death).

**Usage:**
- Examine which comorbidities, when present with AP, may increase the risk of fatal outcomes in patients.

