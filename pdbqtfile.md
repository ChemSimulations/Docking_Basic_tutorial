### Preparing a PDBQT file from PDB file

1. Download the pdb file with PDB ID [8GCY](https://www.rcsb.org/structure/8GCY) from the [RCSB](https://www.rcsb.org/).
2. Type ADT (autodock tools) in the windows search bar and open it. ADT GUI will be popped up
3. To prepare a grid box, find out the center of mass of ligand and get its X, Y, Z coordinates.
4. You can calculate center of mass of the ligand in VMD (easy) or python scipting.
5. Open the pdb file (8GCY) in the VMD viewer or pymol and remove all the solvent molecules, Sulphaate molecules, Zinc molecules and other molecules.
6. Command to remove water molecule in pymol: remove resn HOH
7. Command to remove sulphate molecule in pymol: remove resn SO4
8. Now save the molecule as 8GCY_clean.pdb
9. Alternatively, in VMD you can select protein and resname Z3N in the representations box. Save the selection as 8GCY_clean.pdb file.
  ![image](https://github.com/user-attachments/assets/20d6a291-2141-4aa8-9588-9f568ef2e7fa)

11. Open the 8GCY_clean.pdb molecule in VMD, and go to --> extensions --> TkConsole.
12. In the Tkconsole type
    ``` set sel[atomselect top "resn Z3N"]```
13. Type the below command to get the center of mass coordnates ```set com[measure center $sel weight mass]```
14. Save the x,y,z coordinates obtained in the notepad.
15. Open the 8GCY_clean.pdb file the autodocktools.
16. **Creating PDBQT file from pdb**
17. 
a) load just protein.pdb file in ADT, click ```EDIT--> ATOMS--> Assign AD4 type```; ```EDIT --> compute gastegier charges;``` ```EDIT-->Hydrogens--> Merge Non-polar```

b) After running all the steps save the file as protein.pdbqt

18. **Preparing a GPF file**
    
    a. Open ADT tools and load the protein pdbqt file and select option grid --> Macromolecule--> Select protein;
    
    b. Go to Gridbox --> give x, y,z grid dimensions; File--> output griddimesnions to file; save current selection
    
    c. Grid -->output-->save GPF (give gpf file name protein.gpf)
