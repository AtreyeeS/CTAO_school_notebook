## Install Gammapy

For convenience we provide a pre-defined conda environment file, so you can get additional useful packages together with Gammapy in a virtual isolated environment. First install Miniconda and then just execute the following commands in the terminal:

```
curl -O https://gammapy.org/download/install/gammapy-1.2-environment.yml
conda env create -f gammapy-1.2-environment.yml
conda activate gammapy-1.2
```

If you are having issues, delete the `sherpa` entry from the environment file.
It is an optional dependency and not required for these tutorials.
If you want, you can install it via pip later, `pip install sherpa`

Now, get the datasets to use in the tutorials.
```
gammapy download notebooks
gammapy download datasets
```

Set a $GAMMAPY_DATA path in your environment
```
conda env config vars set GAMMAPY_DATA=$PWD/gammapy-datasets/1.2
