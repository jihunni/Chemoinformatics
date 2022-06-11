# summary for Autodock Vina
1. choose the protein target and ligand molecule
2. carry out protein and ligand preparation
3. select the docking site in protein
4. Carry out protein-ligand docking using docking tool
5. different ligand poses are generated.

# Steps in Autodock Vina
Ref : https://www.youtube.com/watch?v=Sux91FJ3Xe8  
Ref : https://www.youtube.com/watch?v=vU2aNuP3Y8I  
## Preparation
1. Download and install MGL Tools (http://mgltools.scripps.edu/downloads)
2. Run the setup , it will take few minutes.
3. After that download AUTODOCK Vina and PYMOL using these links http://vina.scripps.edu/index.html
         https://pymol.org/2/
4. AUTODOCK is used for molecular docking, in which we search for the appropriate ligand for the protein.
5. RCSB PDB Database is used for PDB structures of the proteins and PubChem used for downloading the Ligand.

## Protein
6. Open the protein structure in AUTODOCK Tools.
7. Now you need to prepare the protein to interact with the ligand.
8. Delete all the water molecules from the structure and add polar hydrogen residues.  
	Edit-Hydrogens-add-polar only
9. Now add kollman charges to have a best possible protein ligand interaction.  
	Edit-Charge-Kollman charges
10. Convert SDF File into PDB to load it in AUTODOCK Tool using PYMOL.  
	grid-macromolecule-choose
## Ligand
11. Prepare the ligand file by following the steps.
	PyMol - Open a file - File - export a molecule - selection molecule - save as 'pdb'  
	Drag pdb file into AutoDockTools  
	Ligand - Input - select - ligand  
	Ligand - output - save as PDBQT  
12. Prepare the Grid, load the protein file and a ligand file.

13. Open the Grid box, it will show exact location where the docking will take place.  
	Grid - Grid box - File - Output grid dimension file
14. Open the command line, give it the path of your folder file.
15. Prepare config.txt file to have all the dimensions.
16. Now run the command 
```
cd C:\Users\user\Desktop\docking
"\Program Files (x86)\The Scripps Research Institute\Vina\vina.exe" --receptor 4mzi.pdbqt --ligand ligand.pdbqt --config config.txt --log log.txt --out output.pdbqt 
```
17. It will generate the log.txt file which will tell the docking score

# QnA
- grid box setting : 
	- https://github.com/ccsb-scripps/AutoDock-Vina/issues/24
	- http://www.bch.cuhk.edu.hk/kbwong/teaching/autodock/autodock.html 
