# Computational-Approaches-in-Drug-Discovery_-Course_2026
All Asignements 
Uploaded Assignments:
 Assignment 1: BENSALEK_Rihab_Task1 (PDB 20 Target Extraction related to colorectal cancer)
 Assignment 2: QSAR_PART1 (DATA Curation- Retrieval and Pre-processing) using Google Colaboratory

Assignment 2 workflow:
 Selected target: EGFR
 Number of Bioactivity Records (IC50): 97
 
 Workflow steps:
1.	Computational environment setup
Google Drive is mounted in Google Collaboratory to allow permanent storage and organized file management.

2.	Installation and import of required Libraries
Required software packages are installed and located to enable database querying and data manipulation.

3.	Target Identification
The biological target is queried in the ChEMBL database and the most relevant target entry is selected using its unique identifier (ID)

4.	Bioactivity data retrieval
All bioactivity records associated with the selected target (“EGFR”) are retrieved and filtered to retain only IC50 measurements.

5.	Raw dataset archiving
The retrieved dataset is saved as a raw CSV file and stored in Google Drive to preserve original integrity.

6.	Initial data quality check/ Data quality assessment
Missing values are inspected to identify potential data quality issues.

7.	Filtering for valid bioactivity measurements
Records without valid numeric IC50 values are removed to ensure analytical reliability.

8.	Preliminary bioactivity classification
Compounds are categorised into active, intermediate and inactive classes based on IC50 thresholds 
•	Active: ≥ 1000 nM
•	Intermediate: > 1000 and < 10000 nM
•	Inactive: ≤ 10000 nM

9.	Feature extraction
Relevant fields were extracted: 
•	Molecule identifier “molecule_chembl_id”
•	Chemical structure “canonical_smiles”
•	Bioactivity value “standard_value”
•	Assigned bioactivity class

10.	Construction of the curated dataset
Extracted variables were assembled into a structured dataframe representing the curated bioactivity dataset.

11.	SMILES Quality Control
Compounds with missing, empty or invalid SMILES strings were removed, this ensured that all remaining compounds possessed valid chemical structures suitable for downstream modelling. 

12.	Saving the Pre-processed Dataset
The cleaned dataset was saved as: “bioactivity_preprocessed_data.csv”
The file was then copied to Google Drive for persistent storage and reproducibility.
