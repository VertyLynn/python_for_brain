# python_for_brain
Various scripts and jupyter notebooks with python code for brain image analysis and visualization.

### Dependencies

To execute these scripts and jupyter notebooks I've used conda to create an environment and get the necessary libraries:
1. Download and install [Anaconda](https://www.anaconda.com/download/)
1. Create an environment:
```bash
conda env create -f environment.yml
source activate brain_env
```
1. Install necessary packages:
```bash
conda install -n brain_env jupyter ipython numpy scipy scikit-learn nibabel matplotlib
pip install nilearn nipype
```
jupyter nbextension enable --py widgetsnbextension
jupyter nbextension enable --py --sys-prefix ipyvolume

## nilearn_brain_atlases.ipynb

Jupyter notebook with different [nilearn atlases](http://nilearn.github.io/modules/reference.html#module-nilearn.datasets) plots.  
## hagmann_connectome/

Code to download [Hagmann connectome](https://doi.org/10.1371/journal.pbio.0060159), to generate a [NetworkX graph](https://networkx.github.io/documentation/stable/index.html), and to write it to disk in [gpickle](https://docs.python.org/3/library/pickle.html) format. Each node of the graph has its Brodmann Area.