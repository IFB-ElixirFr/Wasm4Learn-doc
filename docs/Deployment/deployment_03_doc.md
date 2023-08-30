# Developpement of Wasm4Learn documentation

## Project layout

```bash
    mkdocs.yml         # The configuration file.
    docs/
        Deployement/   # 
            ...
        Components/    # Component usable in the (md) files
            ...
        index.md       # The documentation homepage.
        ...            # Other markdown pages, images and other files.
```

## Developpement

To work locally with this project, you'll have to follow the steps below:

### Install dependencies

1. Fork, clone or download this project
2. Create and activate conda env

```bash
cd Wasm4Learn-doc
conda env create -f env_docs.yml
conda activate docs
```

### Development Server

1. Preview your project

```bash
mkdocs serve
```

Note : *The site can be accessed under http://localhost:8000/*

2. Add content

Add/update markdown files in docs folder

### Production

1. Test

```bash
mkdocs build
```

2. Deploy

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