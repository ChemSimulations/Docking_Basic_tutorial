1. **Add Vina to the System PATH (Recommended for Frequent Use)**
Add Vina Directory to PATH:

Open System Properties:
Right-click on This PC or My Computer and select Properties.
Go to Advanced system settings > Environment Variables.
Under System variables, find Path, select it, and click Edit.
Add the Vina directory path:
plaintext
Copy code
C:\Program Files (x86)\The Scripps Research Institute\Vina

2. **Four steps requried for autodock vina to run a docking calculations**
   a) Protein.pdbqt file
   b) Ligand.pdbqt file
   c) Grid parameter information

3. To prepare protein.pdbqt file
   a) Open Autodock tools-> File--> ReadMolecule-- A window with 3D protein structure is observed.
   b) Go to EDIT --> Add Hydrogens --> select all Hydrogens
   c) Go to EDIT --> Add hydrogens --> Merge non-polar
   d) Go to EDIT --> Add hydrogens --> choose charges --> Kollman Charges
   e) Total charges is 1.848, we need to make it as integer 1 or 2; no decimal points
   f) Go to EDIT--> choose charges -->check total charges on residues --> Spread charge deficit on all atoms
   e) Go to EDIT --> choose charges --> check total charges on resides --> no charges with integral charges are found
   
