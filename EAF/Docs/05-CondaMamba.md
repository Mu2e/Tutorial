# Using Conda/Mamba

Conda is an open-source Python package and environment management tool. Mamba is a `C++` implementation of Conda: it has the same command syntax but is supposed to be more efficient. We will use it to control our Python environment. To initialise:

1. Configure your `.bash_profile` using any text editor (such as `emacs` or `vim`):

   ```bash
   # Add to ~/.bash_profile
   if [ -f ~/.bashrc ]; then
       . ~/.bashrc
   fi
   ```

2. Initialise Mamba:

   ```bash
   mamba init
   ```

Ensure that you either start a new shell after initialisation, or run 

```bash
source ~/.bashrc
```

## Basic Conda/Mamba commands 

Below is a list of basic Conda/Mamba commands. You should **not** need to use most of these.

### Environment management

```bash
# Activate an environment
mamba activate myenv

# Deactivate current environment
mamba deactivate

# List all environments
mamba env list

# Remove a environment by name
mamba env remove -n myenv

# Export environment to YAML file
mamba env export > env.yml

# Create environment from YAML file
mamba env create -f env.yml

# Create a new named environment
mamba create -n myenv

```
### Package management

```bash
# Install a package
mamba install package_name

# Install multiple packages
mamba install package1 package2

# Remove a package
mamba remove package_name

# Update a specific package
mamba update package_name

# Update all packages
mamba update --all

# List installed packages
mamba list

# Search for a package
mamba search package_name
```

### General

```bash
# Initialise Mamba
mamba init

# Clean cache (downloaded packages)
mamba clean

# Display Mamba system information
mamba info
```      

## Navigation

- Previous: [Navigating JupyterHub](04-JupyterHub.md)
- Next: [The Mu2e Python Environment](06-TheMu2eEnvironment.md)
- [Back to Main](../README.md)