# Pymol_Scripts_Commands

List of Pymol commands frequently used:

1. RMSD Calculation:
   a. heavy atom:
     ```
     align mobile & not name H* , target & not name H* , cycles=100, transform=1
     ```
   b. Backbone
     ```
     align mobile & name P+OP1+OP2+O5'+O3'+C1'+C2'+C3'+C4'+O4' , target & name P+OP1+OP2+O5'+O3'+C1'+C2'+C3'+C4'+O4' , cycles=100, transform=1
     ```
2. Post docking see interactions between ligand and receptor
   ```
   # Select residues within 5 Å of ligand
   select near_residues, (byres (organic around 5))

   # Show only ligand ↔ residue interactions (no internal ones)
   dist interactions, organic, near_residues, mode=2
```
