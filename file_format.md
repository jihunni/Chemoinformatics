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

# visualization software
- Avogadro
- VMD
