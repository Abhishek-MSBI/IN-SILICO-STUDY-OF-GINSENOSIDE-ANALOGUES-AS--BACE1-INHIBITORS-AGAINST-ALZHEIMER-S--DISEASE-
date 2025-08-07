# In Silico Study of Ginsenoside Analogues as BACE1 Inhibitors Against Alzheimer's Disease
This repository contains the data and report for a Master of Science in Bioinformatics project conducted at Garden City University. The study focuses on the computational identification and characterization of ginsenoside analogues as potential inhibitors of Beta-site APP Cleaving Enzyme 1 (BACE1), a key therapeutic target in Alzheimer's Disease.

## Project Description
Alzheimer's disease (AD) is a devastating neurodegenerative disorder with a significant global health impact. The "amyloid hypothesis" posits that the accumulation of amyloid-beta (Aβ) peptides is a primary driver of the disease. BACE1 is the rate-limiting enzyme responsible for producing these Aβ peptides, making it a prime target for therapeutic intervention. However, numerous BACE1 inhibitors have failed in late-stage clinical trials, often due to a combination of safety concerns and a lack of clinical efficacy, despite successfully lowering Aβ levels.

This project explores natural products, specifically ginsenosides from Panax ginseng, as a source of novel chemical scaffolds for BACE1 inhibition. It leverages a multi-step in silico workflow to screen for promising candidates, analyze their binding mechanisms, evaluate their drug-like properties, and assess the dynamic stability of the top-ranked protein-ligand complex.

## Methodology
The computational pipeline involved the following key steps:

Ligand Selection: Ginsenoside analogues were selected from the ChEMBL database based on 80-90% similarity to the reference structure, ginsenoside Rg1 (CHEMBL501637). Donepezil (an existing AD drug) and Verubecestat (a clinical BACE1 inhibitor) were used as reference compounds.

Protein and Ligand Preparation: The BACE1 receptor structure (PDB ID: 1FKN) and all ligand structures were prepared using BIOVIA Discovery Studio and UCSF Chimera. This involved adding hydrogens, removing water molecules, assigning charges, and energy minimization.

Molecular Docking: Virtual screening was performed using AutoDock Vina (interfaced via Pyrx) to predict the binding affinities and poses of the ginsenoside analogues within the BACE1 active site.

Interaction Analysis: The top-ranked complexes were visualized using PyMOL, and the specific non-covalent interactions (e.g., hydrogen bonds, hydrophobic contacts) were analyzed in detail with BIOVIA Discovery Studio.

ADMET Profiling: The SwissADME web server was used to predict the Absorption, Distribution, Metabolism, Excretion, and Toxicity (ADMET) properties of the lead candidate and reference drugs to assess their pharmacokinetic viability and drug-likeness.

Molecular Dynamics (MD) Simulation: A 1-nanosecond all-atom MD simulation was performed on the top-ranked BACE1-ligand complex to evaluate its dynamic stability and the persistence of key interactions over time.

## Key Findings
Several ginsenoside analogues demonstrated high predicted binding affinities for BACE1, with the top candidate, CHEMBL3594353, showing a binding energy of -9.7 kcal/mol, which is more favorable than the reference drugs Verubecestat (-8.3 kcal/mol) and Donepezil (-8.3 kcal/mol).

The lead candidate forms extensive interactions with key residues in the BACE1 active site, including hydrogen bonds and significant hydrophobic contacts.

MD simulations confirmed that the BACE1-CHEMBL3594353 complex is structurally stable, with the ligand remaining securely bound in the active site and inducing a rigidification of the functionally important "flap" region of the enzyme.

Despite its high predicted potency, the ADMET analysis revealed that CHEMBL3594353 has significant pharmacokinetic liabilities, including a high molecular weight, poor predicted gastrointestinal absorption, and an inability to cross the blood-brain barrier, highlighting major challenges for its development as a CNS drug.

## Software and Dependencies
Databases: ChEMBL, PubChem, ZINC, Protein Data Bank (PDB)

Modeling & Preparation: BIOVIA Discovery Studio v4.5, UCSF Chimera v1.13

Docking: AutoDock Vina v4.2.1, Pyrx, Open Babel

Visualization: PyMOL v2.3.2

ADMET Analysis: SwissADME

## Author Information
### Student Researcher: Abhishek S R (24MSBI155)

### Project Guide: Dr. VG Shanmuga Priya (Associate Professor)

### Institution: Department of Life Sciences, Garden City University, Bengaluru, India

License
This project is licensed under the MIT License. See the(LICENSE) file for details.

Copyright (c) 2025 Abhishek S R

