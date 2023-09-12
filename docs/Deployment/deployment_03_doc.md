# Developpement of Wasm4Learn documentation

## Project layout

```bash
    mkdocs.yml                  # The configuration file.
    docs/
        Deployement/            # contains the .md files for the deployement of each repository
            deployement_01_.md
            deployement_02_.md
            ...
            images/             # images used in the .md files
        Components/             # exemples of the component usable in the .md files
            componenets_01_.md
            componenets_02_.md
            ...
        index.md                # The documentation homepage.

```

## Setup

To work locally with this project, you'll have to follow the steps below:

### Step 1
Fork, clone or download this project

```bash
git clone git@github.com:IFB-ElixirFr/Wasm4Learn-doc.git
```

### Step 2
Create a conda env

```bash
cd Wasm4Learn-doc
conda env create -f env_docs.yml
```

### Step 3
Activate the environment and you are good to go:

```bash
conda activate docs
```

## Step 3 

- Preview your project

```bash
mkdocs serve
```

!!! note
    The site can be accessed under `http://localhost:8000` 

- Add content

Add/update markdown files in docs folder

### Production

1. Test/build the documentation site

    ```bash
    mkdocs build
    ```

2. Deploy the site on the github pages

    **Only if the previous command is Ok !**

    ```bash
    mkdocs gh-deploy --force
    ```

If you add an extension to (Material) MKdocs that requires the installation of a new package.
Don't forget to export the conda environment (env_docs.yml) using the command line below.

```bash
conda env export --no-builds env_docs.yml
```

Read more at:

- MkDocs [documentation](https://www.mkdocs.org/)
- Mkdocs Material [documentation](https://squidfunk.github.io/mkdocs-material/)