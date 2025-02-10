# Using Conda/Mamba

Conda is an open-source package and environment management system. Mamba is a `C++` implementation of Conda: it has the same command syntax but is supposed to be more efficient. To initialise:

1. Configure your`.bash_profile`:
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
   Start a new shell after initialisation.

## Navigation

- Previous: [Navigating JupyterHub](04-JupyteHhub.md)
- Next: [The Mu2e Python Environment](06-TheMu2eEnvironment.md)
- [Back to Main](../README.md)