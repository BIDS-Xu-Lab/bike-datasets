# BIKE Datasets

The actual datasets are hosted at https://huggingface.co/datasets/medviz/bike-datasets

Due to the large size of data files, please install `git-lfs` and enable it first before downloading the data files.

# Development

Install `git-lfs`:

```
brew install git-lfs
git lfs install
```

Add your SSH key to HuggingFace https://huggingface.co/settings/keys.

Then you can download the dataset from HuggingFace.

```
git clone git@hf.co:datasets/medviz/bike-datasets
```

After downloading this repo, check the file size in the `data/medviz` folder.
The file size of those `.tsv` files should be quite large. If not, usually it's caused by missing of `git-lfs`

<img width="457" alt="image" src="https://github.com/user-attachments/assets/350524d1-b9db-444e-9dd7-db296161b055">

# Server

TBD

# File Format

To ensure the loading by frontend, the `.tsv` file must be in the correct format:

```
pid, title, abstract, journal, year, mesh_terms, color, x, y, size
```

The `mesh_terms` column should be a list of keywords seperated by `;`, for example: `Infections;Kidney;Kidney Diseases;Microscopy, Electron;Poultry Diseases;Specific Pathogen-Free Organisms`
