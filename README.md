# DBlink
### Welcome to DBlink github page
![Alt Text](https://github.com/alonsaguy/DBlink/blob/main/gif_recon_vs_blinks_slower.gif)

Disclaimer:

This repository is based on the following paper: "Dblink: Dynamic localization microscopy in super spatiotemporal resolution via deep learning".

Please also cite the original [paper](https://www.biorxiv.org/content/10.1101/2022.07.01.498428v1) when using or developing this notebook.

Files description:
* demo.py - contains training and testing schemes
* NN_model.py - contains the pytorch model of our network
* Trainers.py - contains the neural network trainer class
* Data_handlers.py - contains data simulators and dataloader classes
* Utils.py - contains helper functions for all files
* exp_params.py - contains the experimental parameters, e.g. pixel size, video crop position and size, etc.

## Installation

First clone the repository and enter the folder.
`git clone https://github.com/alexschroeter/DBlink/`
`cd DBlink`

### UV / PIP

1. Setup the virtual environment of your choice. Python 3.10 is needed for recent PyTorch using AMD GPUs.

    `uv venv --python 3.10` or `python -m venv .venv`

2. Install the flavor of pytorch relevant to your system
    
    a. Cuda (Nvidia)

    `uv pip install torch torchvision` or `pip install torch torchvision`
    
    b. ROCm (AMD)

    `uv pip install torch torchvision --index-url https://download.pytorch.org/whl/rocm6.4`or `pip install torch torchvision --index-url https://download.pytorch.org/whl/rocm6.4`

3. Install everything else using the `pyproject.toml`.

    `uv pip install .` or `pip install .`

### Conda

You can use the provided `environment.yaml` to set up your conda environment.

