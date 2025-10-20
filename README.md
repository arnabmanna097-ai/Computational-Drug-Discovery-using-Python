# Computational-Drug-Discovery-using-Python
This project demonstrates how computational methods and cheminformatics tools can accelerate the early stages of drug discovery, using bioactivity data from ChEMBL and molecular descriptor analysis via RDKit.

📁 **Project Overview**

**This work is divided into two main parts:**

**Part 1: Download & Curate Bioactivity Data**

Retrieve target and bioactivity data from ChEMBL using the chembl_webresource_client API.

Filter data for a coronavirus-related protein target (CHEMBL4523582, SARS-CoV-2).

Extract compounds with IC₅₀ values (in nM) relevant to bioactivity screening.

Handle missing data and remove structural duplicates (canonical_smiles).

**Label compounds as:**

Active: IC₅₀ < 1000 nM

Inactive: IC₅₀ > 10,000 nM

Intermediate: 1000 ≤ IC₅₀ ≤ 10,000 nM

Export the curated dataset as Bioactivity_data_curated.csv.

**Part 2: Exploratory Data Analysis (EDA)**

Install and use RDKit to compute Lipinski’s Rule of Five molecular descriptors:

Molecular Weight (MW)

LogP (octanol-water partition coefficient)

Hydrogen Bond Donors (HBD)

Hydrogen Bond Acceptors (HBA)

Convert IC₅₀ values to pIC₅₀ (−log₁₀(IC₅₀)) for better data distribution and scaling.

Normalize extreme IC₅₀ values (>10⁸ nM) to avoid negative logarithmic results.

Combine all descriptors and activity classes into a unified DataFrame.

Visualize compound distribution and class balance using Matplotlib and Seaborn.

🧰 **Tools & Libraries**
Data Access:	chembl_webresource_client
Data Handling:	pandas, numpy
Molecular Descriptors:	rdkit
Visualization:	matplotlib, seaborn
Environment	Python: Google Colab Notebook)

📊 **Key Results**

Retrieved and curated bioactivity data for SARS-CoV-2 protein targets.

Computed Lipinski descriptors to evaluate drug-likeness.

Generated pIC₅₀-transformed datasets to support quantitative structure–activity relationship (QSAR) modeling.

Conducted EDA visualizations showing relationships between activity class and molecular properties.

💡 **Insights**

This project highlights how integrating computational chemistry and data science can streamline the preclinical drug discovery workflow by:

Reducing experimental cost and time.

Prioritizing active compounds for downstream testing.

Establishing reproducible, data-driven approaches to medicinal chemistry.

📂 **Files in this Repository**
1. Computational Drug Discovery [Part 1] Download Bioactivity Data.ipynb
2. Computational_Drug_Discovery_[Part_2]_Exploratory_Data_Analysis.ipynb



**Arnab Manna**

💼 Aspiring Bioinformatics & Data Science Researcher

📫 LinkedIn Profile
 (https://www.linkedin.com/in/arnab-manna-b41297190/)

🧠 **Keywords**

Computational Drug Discovery · ChEMBL · Cheminformatics · Bioinformatics · RDKit · Lipinski · pIC50 · Python
