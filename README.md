

This repository contains supporting tables for the study in machine-readable **Excel Open XML spreadsheet format** (`.xlsx`) and **Comma Separated Vector format** (`.csv`). These data files are freely available to fulfill public access requirements (e.g., DOE policy) and supplement a journal publication.

---

## 📄 Table S1 – Chemical Space Explored

- **Columns A–D**: Code names, SMILES, full names, IUPAC names  
- **Column E**: Aggregate state at 25 °C (liquid/solid)  
- **Column F**: Chemical class (note: can be ambiguous in multifunctional molecules)  
- **Column G**: Density in kg/m³ (for liquids, if known)  
- **Column H**: Whether the molecule was measured (1 = yes, 0 = no)  
- **Column I**: Initial K-means cluster (8 clusters based on descriptor vector distances)  
- **Columns J–M**: Projections on the first four principal components (PC1–PC4)  
- **Column N**: CAS number  
- **Column O**: Purity  
    - `[1]` = Dried over molecular sieves  
    - `[2]` = HiPerSolv CHROMANORM (HPLC grade)  
- **Column P**: Source of the compound  

---

## 📄 Table S2 – Step-1 Kinetic Data Summary

- **Columns A–F**: Code names, SMILES, chemical names, class, molecular weight (g/mol), density (kg/m³)  
- **Column G**: MPT-BF₄ molarity in MeCN  
- **Column H**: Second-order rate constant *k₂* (units: h⁻¹ in stock concentration)  
- **Column I**: Relative error in rate constant (standard deviation)  
- **Column J**: Stock dilution factor (solids only)  
- **Column K**: Stock molarity  
- **Column L**: *k₂* converted to h⁻¹ M⁻¹  
- **Column M**: log(*k₂*)  
- **Column N**: SQL database entry (tracking step-1 iteration progress)  

> Note: Long-lived reagents not reacting within the time frame in dilute MeCN were excluded and instead tested in step-2 trials (Table S3).

---

## 📄 Table S3 – Step-2 Kinetic Data Summary

- **Columns A–D**: Solvent code name, SMILES, full name, chemical class  
- **Column E**: Step-1 “slow” flag  
- **Column F**: Stability rank  
  - Rank 0 = projected *t*₁⁄₂ < 100 h  
  - Ranks 1–6 = projected *t*₁⁄₂ > 1500 h to > 100 h  
- **Columns G–L**: Projected *t*₁⁄₂ ranges  
- **Column M**: Diluent used (FEC or MeCN)  
- **Column N**: Fractional composition (volume or weight)  
- **Columns O–P**: Projected lifetimes in steps 2 and 3  
- **Column Q**: Plate code  
- **Column R**: Model classification:  
    - `Linear` = extrapolated *k₂* < water  
    - `*` = introduced from step-1  
- **Column S**: LGR model prediction (`pos` = >100 h)  
- **Columns T–U**: Machine learning model selections for >1000 h candidates  
    - LGR = logistic regression  
    - rf = random forest  

---

## 📄 Table S4 – Step-3 Kinetic Data Summary

- **Columns A–D**: Solvent name, SMILES, full name, chemical class  
- **Column E**: Solution composition  
- **Column F**: Linearly projected *t*₁⁄₂ (h)  
- **Column G**: Plate code  
- **Column H**: Fit type (single/double exponential)  
- **Column I**: Observation time frame  
- **Column J**: Survival rate at experiment end  
- **Columns K–V**: Data reduction tuples (f_ν, tau_ν, delta_taû_ν)

> Asterisks mark extrapolated time values.

---

## 📄 Table S5 - Candidates for > 1,000 h Solvents Found Through Search Space Expansion (550 Molecules)

- **Column A**: The first letter of a numbered molecule in column A corresponds to a series in the first column Table S4.3.
- **Columns B-D**: SMILES structural formulas, IUPAC names, and CAS registry numbers



