# The Mu2e Python environment

To ensure that users have immediate access to the libraries and tools needed to conduct analysis, we have installed a Mu2e Python environment on `/cvmfs` that can used on **both** EAF and the virtual machines. It also features an in-built kernel, so the environment can be used interactively. 

## Use on EAF

To set up the environment on EAF:

1. Create an environment symlink to the `current` version:
   ```bash
   ln -s /cvmfs/mu2e.opensciencegrid.org/env/ana/current ~/.conda/envs/mu2e_env
   ```

2. Activate the environment:
   ```bash
   mamba activate mu2e_env
   ```

## Use on the `gpvms`

To activate the environment, first run `mu2einit` and then **one** `pyenv` command, like

```
mu2einit # or "source /cvmfs/mu2e.opensciencegrid.org/setupmu2e-art.sh"
pyenv ana # Setup the current environment
pyenv rootana # Setup the current environment, plus ROOT for pyROOT users 
pyenv ana 1.2.0 # Setup a specific version
pyenv -h # Get help (--help and pyenv with no flag will also return help)
```

If `pyenv` does not work, please source the activation script directly, as shown below, and report the issue to Sam Grant.

```
source /cvmfs/mu2e.opensciencegrid.org/env/ana/current/bin/activate
```

Also note that `mu2einit` should be aliased to `source /cvmfs/mu2e.opensciencegrid.org/setupmu2e-art.sh` in your `~/.bashrc` (or `~/.my_bashrc`).

When using alongside `muse`, it is advisable to run the activation script after `muse setup` to ensure that your environment variables are set correctly. 

```bash
mu2einit
muse setup ops
pyenv ana # or source /cvmfs/mu2e.opensciencegrid.org/env/ana/current/bin/activate
```

## Interactive use 

Environment versions >=1.2.0 include an in-built interactive kernel, called `mu2e_env`, which is available automatically. See the following exercise for more information! 

## Packages

As of `v2.0.0`:

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
- tdqm 
- hist
- **pyutils (Mu2e Python utilties)** 

Environment versions <2.0.0 contain the deprecated [`anapytools`](https://github.com/Mu2e/anapytools.git), rather than [`pyutils`](https://github.com/Mu2e/pyutils.git). See the [pyutils section](08-pyutils.md) for more information.

Also see the [wiki](https://mu2ewiki.fnal.gov/wiki/Elastic_Analysis_Facility_(EAF)#The_Mu2e_environment) for details on the various versions of the Mu2e Python environment.



## Navigation

- Previous: [Using Conda/Mamba](05-CondaMamba.md)
- Next: [Exercise: "Hello world!"](07-HelloWorld.md)
- [Back to Main](../README.md)