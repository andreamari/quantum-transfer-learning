
# Supplementary numerical simulations
In the review process of the work [arXiv:1912.08278](https://arxiv.org/abs/1912.08278), it was suggested to make some additional numerics with the aim of clarifying the relationship our quantum machine learning models with respect to classical methods.
In this folder we share this material since it could be of some interest also to other researchers and quantum programmers.


## Contents
* `dressed_circuit_different_shape.ipynb`: Jupyter notebook where a dressed quantum circuit is used to classify a non-linearly separated dataset of points. Differently from the spiral shape used in [arXiv:1912.08278](https://arxiv.org/abs/1912.08278), in this notebook different distributions of points are used.

* `direct_classification_with_RESTNET18.ipynb`: Jupyter notebook where the ResNet18 network, which in the notation of [arXiv:1912.08278](https://arxiv.org/abs/1912.08278) is called network _A_, is directly used to classify images of _ants_ and _bees_. 

* `transfer_learning_ants_bees_classical.ipynb`: Jupyter notebook where the ResNet18 network, which in the notation of [arXiv:1912.08278](https://arxiv.org/abs/1912.08278) is called network _A_, is modified by removing the final layer to obtain a shorter network _A'_ with 512 output nodes. In order to adapt the output nodes of _A'_ to the specific classification of  _ants_ and _bees_, a final classical layer with with 2 output nodes is appended to _A'_ and trained for this task.


## Usage

To visualize the content of the Jupyter notebooks without running the code there are two alternatives:
1. Navigate with a browser to the GitHub repository and simply click on the notebook file. GitHub will automatically visualize the notebook, however the rendering may not be good (especially for LaTeX formulas).
2. Copy the URL of the notebook file and paste it into [nbviewer](https://nbviewer.jupyter.org).

To open and run a local copy of a notebook one should apply the following steps:

1. If missing, install [JupyterLab or Jupyter Notebook](https://jupyter.org/install).
2. Run the command:
```
$ jupyter notebook
```
3. Navigate to the local notebook file and open it.


## Requirements

#### Software
The library matplotlib is required for generating plots and images.

The notebook `dressed_circuit_different_shape.ipynb` requires the Python library PennyLane.

The other notebooks require the Python libraries PennyLane and PyTorch.
They also require to manually download the dataset, consisting of the _Hymenoptera_ subset of ImageNet (ants and bees). The dataset can be downloaded [here](https://download.pytorch.org/tutorial/hymenoptera_data.zip) and should extracted in the subfolder `..\data\hymenoptera_data\`

