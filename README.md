# chemoinformatics Reference
- RDKit - 강의 1 + Mol Mol2 포맷 | [youtube](https://www.youtube.com/watch?v=sxj56IQqhqM&list=PL30UV7ug7LwJYQgSp4THPjlb-9XAV4DCe&ab_channel=Prof.J.Lee)
- RDKit 강의 - Molecular Descriptors, Druglikeness, ADMET, logP | [youtube](https://www.youtube.com/watch?v=SZzfljEo4ec&list=PL30UV7ug7LwJYQgSp4THPjlb-9XAV4DCe&index=5&ab_channel=Prof.J.Lee)
- https://www.rdkit.org/docs/GettingStartedInPython.html
- https://www.rdkit.org/docs/Cookbook.html

# paper
- Large-scale comparison of machine learning methods for drug target prediction on ChEMBL
- MoleculeNet: A Benchmark for Molecular Machine Learning
## Molecular dynamics
- Exploring Transition Pathway and Free-Energy Profile of Large-Scale Protein Conformational Change
  - Exploring Transition Pathway and Free-Energy Profile of Large-Scale Protein Conformational Change by Combining Normal Mode Analysis and Umbrella Sampling Molecular Dynamics
  - Molecular Dynamics Study of Conformational Changes of Tankyrase 2 Binding Subsites upon Ligand Binding
# library
- ASE (Atomic Simulation Environment)

# database
- ZINC database
- PubChem | [link](https://pubchem.ncbi.nlm.nih.gov/) 
  - largest database 
  e.g. aspirin - download `SDF` format
    - Although 3D position of a simple molecule can calculated with VSEPR, it is not accurate for complex atom. Atomic position in 3D requires the sophisticate calculation with quantum chemistry.
- ChEMBL database  
  - chmicals with biological reacticity
- Quantum chemistry structures and properties of 134 kilo molecules
- KEGG DRUG Database | [link](https://www.genome.jp/kegg/drug/)
  - Download DB
    Ref : https://www.biostars.org/p/48319/
    - Get an ftp client
    - Go to `ftp://ftp.genome.jp/pub/kegg/medicus/`
    - Go into the drug directory
    - Download the file called drug, that is the database in DBGET format. You can write your own scripts to turn it into a database. 
- LigandBox | [link](http://www.mypresto5.com/ligandbox/cgi-bin/index.cgi?LANG=en)
- ExCAPE database
- FDA Adverse Report System (FAERs): drug-side effect 
- Side Effect Resource (SIDER) : drug-side effect 
- ClassyFire : structure-based chemical taxonomy

# Web service
- The GlycoBioChem PRODRG2 Server: PRODRG will take a description of a small molecule (as PDB coordinates / MDL Molfile / SYBYL Mol2 file / text drawing) and from it generate a variety of topologies for use with GROMACS, WHAT IF, Autodock, HEX, CNS, REFMAC5, SHELX, O and other programs, as well as energy-minimized coordinates in a variety of formats.

# Drug discovery
## Methods for Drug Combination Analysis
Ref: https://www.youtube.com/watch?v=VwYPuQZIMLY&ab_channel=PrecisionHealth
- dose-effect-based analysis
  - combination subthresholding
  - highest single agent
  - response activity
  - Bliss independence model
- effect-based drug combination
