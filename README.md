# chemoinformatics Reference
- RDKit - 강의 1 + Mol Mol2 포맷 | [youtube](https://www.youtube.com/watch?v=sxj56IQqhqM&list=PL30UV7ug7LwJYQgSp4THPjlb-9XAV4DCe&ab_channel=Prof.J.Lee)
- RDKit 강의 - Molecular Descriptors, Druglikeness, ADMET, logP | [youtube](https://www.youtube.com/watch?v=SZzfljEo4ec&list=PL30UV7ug7LwJYQgSp4THPjlb-9XAV4DCe&index=5&ab_channel=Prof.J.Lee)
- https://www.rdkit.org/docs/GettingStartedInPython.html
- https://www.rdkit.org/docs/Cookbook.html

# Computational modling
- Large-scale comparison of machine learning methods for drug target prediction on ChEMBL
- MoleculeNet: A Benchmark for Molecular Machine Learning
## protein structure alignment
- DALI
- TM-align : [paper](https://academic.oup.com/nar/article/33/7/2302/2401364)

## Molecular dynamics
### Force Field
- Improved side-chain torsion potentials for the Amber ff99SB protein force field
- Development of polyphosphate parameters for use with the AMBER force field
### pKa
- DelPhiPKa Web Server
- H++
### Exploring Transition Pathway and Free-Energy Profile of Large-Scale Protein Conformational Change
  - Exploring Transition Pathway and Free-Energy Profile of Large-Scale Protein Conformational Change by Combining Normal Mode Analysis and Umbrella Sampling Molecular Dynamics
  - Molecular Dynamics Study of Conformational Changes of Tankyrase 2 Binding Subsites upon Ligand Binding
## Deep learning
  - Quantum-chemical insights from deep tensor neural networks
  - SchNet
  - Boltzman generators

## Ab initio protein folding
- Fast and accurate Ab Initio Protein structure prediction using deep learning potentials | 2022


## De novo protein deisgn for receptor-ligand pipeline
- side chain positioning problem : Packer  
  Ref: https://www.rosettacommons.org/node/9563  
  To solve the sidechain positioning problem, Rosetta uses "the Packer". This is a non-deterministic Metropolis Monte Carlo simulated annealing protocol, which attempts to find the lowest energy conformation of sidechains on a fixed backbone, assuming the sidechains come from a fixed set of rotamers.   
  The reason it's called the "packer" is that it was originally developed to find the optimal packing of sidechains in the hydrophobic core of proteins. It turns out that the packer is generally useful for combinitorial optimization of sidechain positioning, and can be used for design as well as packing. (Instead of choosing between rotamers of a single amino acid, you just add in rotamers of other amino acids too - the algorithm is residue-based, so the different number/kinds of atoms in different amino acids doesn't matter.) So sometimes you'll hear talk of "packing" even when the identity of the amino acid is allowed to change.  
- Protein-protein interaction  
  - Docking: 
    - PatchDock
      - `paper` Efficient Unbound Docking of Rigid Molecules
    - RosettaDock  
      - `paper` Protein–Protein Docking with Simultaneous Optimization of Rigid-body Displacement and Side-chain Conformations
      - `paper` Protocols for Molecular Modeling with Rosetta3 and RosettaScripts
      - `tool` DockingPie: [paper](https://academic.oup.com/bioinformatics/article/38/17/4233/6632656) [github](https://github.com/paiardin/DockingPie)
  
### Antibody design
- `review` Modeling Immunity with Rosetta: Methods for Antibody and Antigen Design
- Clustering
  - `paper` A New Clustering of Antibody CDR Loop Conformations
  - `database` PyIgClassify : a monthly-updated web server primarily providing the clusters and associated information of the antibody complementarity determining regions (CDRs) in the Protein Data Bank (PDB). The current database contains 3,065 PDB antibody entries.
  - `paper` Improving Loop Modeling of the Antibody Complementarity-Determining Region 3 Using Knowledge-Based Restraints
  
- Antibody structure prediction : RosettaAntibody, AbPredict, RosetaCM
- Antibody-Antigen Docking: RosettaDock, SnugDock
- Antibody Design
  - Single-state design (affinity maturation): RosettaAntibodyDesign, AbDesign
  - Multi-state design : REstrained CONvergence (RECONV) algorithm, BROAD (BReadth Optimization for Antibody Design) algorithm
- Epitope-focused immunogen design: side chain grafting, backbone grafting, FunFolDes (Functional Folding and Design)
  - `paper (2011)` Computational Design of Proteins Targeting the Conserved Stem Region of Influenza Hemagglutinin   
    - This approach does not make any assumptions about the nature of the hotspot or the scaffold protein. It generate a hotspo region consisting of high-affinity interacting residues of all types and incorporate them into a variety of scaffold proteins. These generalizations allow to design binders of potentially any protein surface.
    - low sucess rate
- Vaccine design through thermostabilization : Protein Repair One Stop Shopt (PROSS)
- Designing and refining glycans: RosettaCarbohydrate framework
- Antigen carrier design

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
- 970 Million Druglike Small Molecules for Virtual Screening in the Chemical Universe Database GDB-13 (REf: https://pubs.acs.org/doi/10.1021/ja902302h)
- Orientations of Proteins in Membranes (OPM) database : [homepage](https://opm.phar.umich.edu/)
- CC+ database | [homepage](http://coiledcoils.chm.bris.ac.uk/ccplus/search/)
- OAS: Observed Antibody Space

# Web service
- The GlycoBioChem PRODRG2 Server: PRODRG will take a description of a small molecule (as PDB coordinates / MDL Molfile / SYBYL Mol2 file / text drawing) and from it generate a variety of topologies for use with GROMACS, WHAT IF, Autodock, HEX, CNS, REFMAC5, SHELX, O and other programs, as well as energy-minimized coordinates in a variety of formats.

# visualization
- Myavi : https://docs.enthought.com/mayavi/mayavi/

# Experiment
- Protein purification
  - Yeast surface display:
    - `protocol` Isolating and engineering human antibodies using yeast surface display
  - nickel-affinity chromatography
    - `paper` : Metal chelate affinity chromatography, a new approach to protein fractionation
  - size-exclusion chromatography
  - to excise a C-terminal stretch (in order to boost surface expression of the design with no significant loss of its functionality)
- Protein-protein interaction
  - surface plasmon resonance (SPR)
  - enzyme-linked immunosorbent assay (ELLISA)
  - Biolayer Interferometry (BLI)
- Affinity maturation
  - site-specific mutagenesis
    - `paper` Rapid and efficient site-specific mutagenesis without phenotypic selection.
- functionality
  - Alanine substitution at core positions
- Structure determination 
  - NMR
  - X-ray crystallography
  - Cryo-electromicroscopy 

# Drug discovery
## Methods for Drug Combination Analysis
Ref: https://www.youtube.com/watch?v=VwYPuQZIMLY&ab_channel=PrecisionHealth
- dose-effect-based analysis
  - combination subthresholding
  - highest single agent
  - response activity
  - Bliss independence model
- effect-based drug combination
