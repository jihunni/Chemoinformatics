# XYZ format
XYZ files contain atomic coordinates. While variants of the format exist, Chimera reads XYZ files that conform to the following:

- First line: total number of atoms (optional)
- Second line: molecule name or comment (optional)
- All other lines: element symbol or atomic number, x, y, and z coordinates, separated by spaces, tabs, or commas

Example:
	```
	12   
	glucose from 2gbp   
	C  35.884  30.895  49.120   
	C  36.177  29.853  50.124    
	C  37.296  30.296  51.074 
	C  38.553  30.400  50.259  
	C  38.357  31.290  49.044  
	C  39.559  31.209  48.082  
	O  34.968  30.340  48.234  
	O  34.923  29.775  50.910  
	O  37.441  29.265  52.113  
	O  39.572  30.954  51.086  
	O  37.155  30.858  48.364  
	O  39.261  32.018  46.920
	```

# PDB format
Ref : https://pdb101.rcsb.org/learn/guide-to-understanding-pdb-data/introduction

# chemical file format
Ref : https://chem.libretexts.org/Courses/University_of_Arkansas_Little_Rock/ChemInformatics_(2017)%3A_Chem_4399_5399/2.2%3A_Chemical_Representations_on_Computer%3A_Part_II/2.2.2%3A_Anatomy_of_a_MOL_file  
- SMILES : 1D string
  Ref : https://www.daylight.com/meetings/summerschool98/course/dave/smiles-isomers.html  
  e.g.   C1(=C(C(=C(C(=C1C2=CC=CC=C2)C3=CC=CC=C3)C4=CC=CC=C4)C5=CC=CC=C5)C6=CC=CC=C6)C7=CC=CC=C7
- Mol file format  
  ![image](https://user-images.githubusercontent.com/48517782/142718373-2383e7db-8fdf-42df-8ada-8fec07e59e40.png)
  - hdeader block
  - atom block : the number of atoms and bonds, 3D coordinates of atoms
  - bond block : 
  - property block
- Mol2 format
  - atom types
  - partial charge
e.g.
```
 OpenBabel10082008492D

 25 26  0  0  1  0  0  0  0  0999 V2000
    0.1340   -1.5000    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
    1.0000   -1.0000    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
    1.0000   -0.0000    0.0000 N   0  3  0  0  0  0  0  0  0  0  0  0
    2.0000   -0.0000 OpenBabel10082008492D

 25 26  0  0  1  0  0  0  0  0999 V2000
    0.1340   -1.5000    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
    1.0000   -1.0000    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
    1.0000   -0.0000    0.0000 N   0  3  0  0  0  0  0  0  0  0  0  0
    2.0000   -0.0000    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
    1.0000    1.0000    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
    0.1340    1.5000    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
    0.0000    0.0000    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -0.5000    0.8660    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -1.5000    0.8660    0.0000 O   0  0  0  0  0  0  0  0  0  0  0  0
   -2.0000    1.7321    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -1.5000    2.5981    0.0000 O   0  0  0  0  0  0  0  0  0  0  0  0
   -3.0000    1.7321    0.0000 C   0  0  3  0  0  0  0  0  0  0  0  0
   -3.0000    2.7321    0.0000 O   0  0  0  0  0  0  0  0  0  0  0  0
   -4.0000    1.7321    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -4.5000    0.8660    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -5.5000    0.8660    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -6.0000    1.7321    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -5.5000    2.5981    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -4.5000    2.5981    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -3.0000    0.7321    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -2.1340    0.2321    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -2.1340   -0.7679    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -3.0000   -1.2679    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -3.8660   -0.7679    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -3.8660    0.2321    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
  1  2  1  0  0  0  0
  2  3  1  0  0  0  0
  3  4  1  0  0  0  0
  3  5  1  0  0  0  0
  3  7  1  0  0  0  0
  5  6  1  0  0  0  0
  7  8  1  0  0  0  0
  8  9  1  0  0  0  0
  9 10  1  0  0  0  0
 10 11  2  0  0  0  0
 10 12  1  0  0  0  0
 12 13  1  0  0  0  0
 12 14  1  0  0  0  0
 12 20  1  0  0  0  0
 14 19  1  0  0  0  0
 14 15  2  0  0  0  0
 15 16  1  0  0  0  0
 16 17  2  0  0  0  0
 17 18  1  0  0  0  0
 18 19  2  0  0  0  0
 20 25  1  0  0  0  0
 20 21  1  0  0  0  0
 21 22  1  0  0  0  0
 22 23  1  0  0  0  0
 23 24  1  0  0  0  0
 24 25  1  0  0  0  0
M  CHG  1   3   1
M  END
$$$$    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
    1.0000    1.0000    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
    0.1340    1.5000    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
    0.0000    0.0000    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -0.5000    0.8660    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -1.5000    0.8660    0.0000 O   0  0  0  0  0  0  0  0  0  0  0  0
   -2.0000    1.7321    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -1.5000    2.5981    0.0000 O   0  0  0  0  0  0  0  0  0  0  0  0
   -3.0000    1.7321    0.0000 C   0  0  3  0  0  0  0  0  0  0  0  0
   -3.0000    2.7321    0.0000 O   0  0  0  0  0  0  0  0  0  0  0  0
   -4.0000    1.7321    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -4.5000    0.8660    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -5.5000    0.8660    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -6.0000    1.7321    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -5.5000    2.5981    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -4.5000    2.5981    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -3.0000    0.7321    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -2.1340    0.2321    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -2.1340   -0.7679    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -3.0000   -1.2679    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -3.8660   -0.7679    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
   -3.8660    0.2321    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
  1  2  1  0  0  0  0
  2  3  1  0  0  0  0
  3  4  1  0  0  0  0
  3  5  1  0  0  0  0
  3  7  1  0  0  0  0
  5  6  1  0  0  0  0
  7  8  1  0  0  0  0
  8  9  1  0  0  0  0
  9 10  1  0  0  0  0
 10 11  2  0  0  0  0
 10 12  1  0  0  0  0
 12 13  1  0  0  0  0
 12 14  1  0  0  0  0
 12 20  1  0  0  0  0
 14 19  1  0  0  0  0
 14 15  2  0  0  0  0
 15 16  1  0  0  0  0
 16 17  2  0  0  0  0
 17 18  1  0  0  0  0
 18 19  2  0  0  0  0
 20 25  1  0  0  0  0
 20 21  1  0  0  0  0
 21 22  1  0  0  0  0
 22 23  1  0  0  0  0
 23 24  1  0  0  0  0
 24 25  1  0  0  0  0
M  CHG  1   3   1
M  END
$$$$
```
- chemical FingerPrints
  - MACCS Key
    frequently used structural pattern  
    e.g. MACCS166  
  - Morgan Algorithm (suggsted by Morgan on 1969)
    ![image](https://user-images.githubusercontent.com/48517782/142729272-4c6b42a7-6977-400e-a913-0adb305ed861.png)  
    1. assign the number of connected atoms as connectivity
    2. sum the connectivity of the connected atoms and assign it as connectivity
    3. Repeat (2) until the connectivity values are not changed.
  - ECFP (most frequently used)
    ![image](https://user-images.githubusercontent.com/48517782/142729858-543a5036-638d-474e-84d8-7dca0cb25cb3.png)  
    1. assign initial numbers to atoms based on the Daylight atomic invariants-derived rule. Initial numbers are put into a hash function. (A hash function is any function that can be used to map data of arbitrary size to fixed-size values. The values returned by a hash function are called hash values, hash codes, digests, or simply hashes.)
      - Number of heavy atom neighbors
      - Atomic number
      - Atomic mass
      - Atomic charge
      - Number of attached hydrogens
      - Whether it is contained in a ring or not
    2. save information of each atom as a list. Get hasn value by using hash function with a list.
    3. iterate 2~3 times
      - ECFP2 : 1 iteration (radius = 1, diameter =2) 
      - ECFP4 : 2 iteration (radius = 2, diameter =4)
      - ECFP6 : 3 iteration (radius = 3, diameter =6)
    4. (optional) Folding to bits to speed up 
      ![image](https://user-images.githubusercontent.com/48517782/142730179-1ec53041-f73d-483a-a685-9eaaeaec627e.png)

- similarity measure with chemical fingerprint
  - Tanimoto Coefficient (Jaccard Index)  
    a similarity measure from two binary vector that ranges from 0 to 1  
    `rdkit.DataStructs.FingerprintSimilarity`
  - Dice similarity  
    `DataStructs.DiceSimilarity`
    
# visualization software
- Avogadro
- VMD
