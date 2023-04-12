To install conda on server, use:

```
# down load conda
wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
# install conda 
sh Miniconda3-latest-Linux-x86_64.sh
```
And activate by: 
```
source ~/.bashrc
```
Now we can create environments by specifying names + python versions:
```
conda create -n language python=3.9
```
The above codes created an environment named **language**, by specifying python version = 3.9

To enter this environment, use:
```
conda activate language
```
And can install packages via pip install/conda install command.

To check the listed packages (installed), use:
```
pip list
# conda list also ok
```

To leave current environment, use:
```
conda deactivate
```

To remove a specific environment (i.e. language), use:
```
conda remove -n language --all
```
Which remove the entire environment with all packages installed.
