# Molecular Graphs

## Environment Managment

### Dealing with SMILE format

The primary package to convert SMILE format to graphs is using  [RDKit](http://www.rdkit.org/docs/api-docs.html).
RDKit has Python API.
It is recomendded to create a separate environment to install this package:

```
conda create -c conda-forge -n my-rdkit-env rdkit
conda activate my-rdkit-env
```

In the same package, after extracting Graph data from SMILE format, it is recomended to use NetworkX for graph visualization according to the following installation:

```
conda install -c anaconda networkx
```

### Pytorch Geometric

Another environment to create is for Pytorch Geometric which is based on Pytorch.
For windows, Pytorch Geometric is not available for 1.13 Pytorch version, you got to have Pytorch 1.12.
Therefore, use the following (according to [Pytorch Doc](https://pytorch.org/get-started/previous-versions/) and [Geometric Pytorch](https://pytorch-geometric.readthedocs.io/en/latest/install/installation.html)):

```
conda create pytorch
conda activate pytorch

# Pytorch Windows CPU Only
conda install pytorch==1.12.1 torchvision==0.13.1 torchaudio==0.12.1 cpuonly -c pytorch

# Geometric Pytorch Windows CPU only
conda install pyg -c pyg
```