
# FEP Benchmarks 

This repo serves 3 purposes:
- stores a reference set of data for ligand-binding systems for bench-marking
- demonstrates the recommended way of storing large sets of simulation data
- provides example scripts to setup up and analyze large sets of simulations

The repo is divided into 4 sections:
- `reference` contains benchmark reference data 
- `scripts` contains all the setup/analysis scripts
- `results` contains all the resultant calculations
- `docs` contains the result `.html` graphs

The graphed results can be viewed at <https://redesignscience.github.io/fep-benchmark/>.

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

## Results

All results of our benchmarking are stored in the `results` directory as `.yaml` files.

`.yaml` files are:

- machine-readable, with libraries available in every language
- human-readable
- encapsulate both hierarchical and list data
- inter-convertible with `.json` files, and web-ready
- mappable to object literals in python

## Docs - graphing the results

The results of our bench-marking are stored in `docs`, which is turned into a URL on gh-pages as:

<https://redesignscience.github.io/fep-benchmark/>

This current set compares the dG of:
- experimental values from the reference data
- bc step from `algdock_rs`
- cd step from `algdock_rs`
- temperdock from `rseed`
- ligand from `rseed`

## Pdb

Prepared structures for all receptor complexes are stored as PDB files in the `pdb` directory. These have been extracted from the `reference` directory.

The structures are ready to simulate, with no water molecules, and the ligand renamed to `LIG`. 

## Methods notes

### Algdock_RS

This is our loose implementation of David Minh's Algdock algorithm, which has 3 steps:

1. mc: pose refinement
2. bc: 300K - 600K replica exchange with ligand in a fixed receptor
3. cd: 600k - 300k replica exchange with ligand in a fixed receptor, with interaction constant between ligand and receptor from 0 to 1.

### Rseed Ligand

Parallel tempering of ligand by itself

### Rseed Temperdock

Parallel tempering of ligand in fixed receptor





