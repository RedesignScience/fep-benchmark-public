
# FEP Benchmarks 

This repo serves 2 purposes:
- stores a reference set of data for ligand-binding systems for bench-marking
- demonstrates the recommended way of storing large sets of simulation data

The repo is divided into 2 sections:
- `reference` contains benchmark reference data 
- `pdb` contains all structures with ligands docked into crystal structures

IC50s from the Christina Schindlers reference set (SDF files) have been extracted and deposited into ic50.yaml, along with the numbering used in the PDB subfolder and the original numbering. Note that an indexing error was identified from the original set and corrected here. 

## Reference Data

This repo stores a major set of benchmarking data for alchemical free-energy calculations. The reference data set in the `reference` directory contains:
 
- 10 receptor systems
- crystal structure
- 20-40 congeneric ligands per receptor
- IC50 measurements 
- computationally-generated docked ligand position 

Reference: 
"Large-Scale Assessment of Binding Free Energy Calculations in Active Drug Discovery Projects
Christina"   
Schindler et al. (2020) J. Chem. Inf. Model  
<https://pubs.acs.org/doi/full/10.1021/acs.jcim.0c00900>

Download source data: <https://zenodo.org/record/3459811#.YoSkgy8RqX3>

## Pdb

Prepared structures for all receptor complexes are stored as PDB files in the `pdb` directory. These have been extracted from the `reference` directory.

The structures are ready to simulate, with no water molecules, and the ligand renamed to `LIG`. 






