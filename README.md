# Hydrophobicity Graph Classifier

This project is about creating a graph neural network that classifies molecular graphs as being hydrophobic or hydrophilic.
The trained model is based on graph convolutional netowork as decribed in [Kipf and Welling (2017)](https://arxiv.org/abs/1609.02907)

## Environment Management

### Dealing with SMILE format

The primary package to convert SMILE format to graphs uses [RDKit](http://www.rdkit.org/docs/api-docs.html).
RDKit has Python API.
It is recommended to create a different environment to install this package:

```
conda create -c conda-forge -n my-rdkit-env rdkit
conda activate my-rdkit-env
```

In the same package, after extracting Graph data from SMILE format, it is recommended to use NetworkX for graph visualization according to the following installation:

```
conda install -c anaconda networkx
```

### Pytorch Geometric

Another environment to create is for Pytorch Geometric, which is based on Pytorch.
For windows, Pytorch Geometric is not available for the 1.13 Pytorch version; you must have Pytorch 1.12.
Therefore, use the following (according to [Pytorch Doc](https://pytorch.org/get-started/previous-versions/) and [Geometric Pytorch](https://pytorch-geometric.readthedocs.io/en/latest/install/installation.html)):

```
conda create pytorch
conda activate pytorch

# Pytorch Windows CPU Only
conda install pytorch==1.12.1 torchvision==0.13.1 torchaudio==0.12.1 cpuonly -c pytorch

# Geometric Pytorch Windows CPU only
conda install pyg -c pyg
```