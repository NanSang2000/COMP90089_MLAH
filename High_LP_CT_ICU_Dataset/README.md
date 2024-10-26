# Lipase_CT_ICU_Patients_Dataset.ipynb

**Description:** This notebook filters ICU patients whose lipase levels are at least three times the normal levels and who were recommended for a CT Scan or Pelvis scan.

# High_Lipase_ICU_Dataset.csv

**Description:** This dataset includes all unique ICU patients with elevated lipase levels, filtered by their `subject_id`. The selection criteria are:
- If a patient has multiple records, only one record is considered. If the patient is deceased, any record can be used; otherwise, the record with the longest length of stay is selected.

# High_Lipase_ICU_Comorbidities_Dataset.csv

**Description:** Derived from the `High_Lipase_ICU_Dataset.csv`, this dataset includes additional diagnosis details, listing all other diseases identified in the same patients to analyze broader health patterns.

# High_Lipase_ICU_CT_Dataset.csv

**Description:** This dataset comprises all unique ICU patients with high lipase levels who have undergone a CT scan or Pelvis scan, filtered by their `subject_id`. The selection criteria are:
- If a patient has multiple records, only one record is considered. If the patient is deceased, any record can be used; otherwise, the record with the longest length of stay is selected.

# High_Lipase_ICU_CT_Comorbidities_Dataset.csv

**Description:** Built on the `High_Lipase_ICU_CT_Dataset.csv`, this dataset includes further diagnoses, identifying additional diseases in the same patients to explore correlations between elevated lipase levels, the need for critical imaging procedures, and other potentially fatal conditions.

