# The Mu2e Python Environment

To ensure that users have immediate access to the libraries and tools needed to conduct analysis, we have an installed a Mu2e Python environment on `/cvmfs`, called `mu2e_env`, that can used on **both** EAF and the virtual machines.

To set up this environment:

1. Create environment symlink:
   ```bash
   ln -s /cvmfs/mu2e.opensciencegrid.org/env/ana/current ~/.conda/envs/mu2e_env
   ```

2. Activate environment:
   ```bash
   mamba activate mu2e_env
   ```

## Available Libraries

- matplotlib
- pandas
- uproot
- scipy
- scikit-learn
- pytorch
- tensorflow
- jupyterlab
- notebook
- statsmodels
- awkward
- urllib3 (v1.26.16)
- ipykernel
- conda-pack
- fsspec-xrootd
- htop
- vector
- plotly
- dash
- anapytools (v2.0.0) 

## Use on Virtual Machines

To use on Mu2e virtual machines:

```bash
# Activate
source /cvmfs/mu2e.opensciencegrid.org/env/ana/current/bin/activate

# Deactivate
source /cvmfs/mu2e.opensciencegrid.org/env/ana/current/bin/deactivate
```

Suggested aliases for `.my_bashrc`:
```bash
alias pystart="source /cvmfs/mu2e.opensciencegrid.org/env/ana/current/bin/activate"
alias pystop="source /cvmfs/mu2e.opensciencegrid.org/env/ana/current/bin/deactivate"
```

When using with `muse`:
```bash
mu2einit
muse setup ops
pystart # or source /cvmfs/mu2e.opensciencegrid.org/env/ana/current/bin/activate
```

## Navigation

- Previous: [Using Conda/Mamba](05-CondaMamba.md)
- Next: [anapytools](07-anapytools.md)
- [Back to Main](../README.md)