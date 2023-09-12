# Developpement of Wasm4Learn

## Project layout

!!! warning
    In public folder, webR files must be duplicated like content r folder

```bash
...
/components
    /content
        ...             # Component usable in content file (md)
    ...                 # content only usable by vue
/composables
    ...                 # function shared in all project
/layouts
    default.vue         # layout of the application
    home.vue            # layout of home page
/pages
    index.vue           # home page
    /language/[lang]/
        index.vue       # home page of language
        [...slug].vue   # How display content
    /learning-path/
        /all/index.vue  # All learning-path available
        [...slug].vue   # How display content
    /tool/[tool]/
        index.vue       # home page of language
        [...slug].vue   # How display content
    about.vue           # About page
    ... 
/plugins                # plugings used by application
    vuetify.js
    markdownit.ts
/publics                # assets available in all web site
    ...
    man/                # Man pages 
/store
    ...                 # Store declaration
nuxt.config.ts          # configuration file
```

## Setup

!!! warning "Requirement"

    Make sure you have already installed ```yarn``` before starting the setup.


### Step 1

Fork, clone or download this project

```bash
git clone git@github.com:IFB-ElixirFr/Wasm4Learn.git
```

### Step 2
Install the dependencies

```bash
cd Wasm4Learn
yarn install
```

### Step 3
Once all the dependencies have been installed, launch the application

```bash
yarn dev
```

If your teminal displays something similar to this:

```bash
Nuxi 3.6.52:54:41 PM
Nuxt 3.6.5 with Nitro 2.5.22:54:41 PM
                                                                                                                                                                                2:54:42 PM
> Local:    http://localhost:3000/Wasm4Learn/ 
> Network:  http://172.16.189.130:3000/Wasm4Learn/

ℹ [content-assets] Websocket listening on "ws://localhost:4001/"   
```

Well done 🥳 !!
the application is now running on `http://localhost:3000` 

### Production

Build the application for production:

```bash
yarn deploy
```
Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.

## Nuxt content and GitHub

Configurate the ```nuxt.config.ts``` file in order for Nuxt content to fetch content from GitHub

```ts
content: {
    sources: {
    github: {
        prefix: '', // Prefix for routes used to query contents
        driver: 'github', // Driver used to fetch contents (view unstorage documentation)
        repo: "IFB-ElixirFr/Wasm4Learn-content",
        branch: "main",
        dir: "content", // Directory where contents are located. It could be a subdirectory of the repository.
        // Imagine you have a blog inside your content folder. You can set this option to `content/blog` with the prefix option to `/blog` to avoid conflicts with local files.
    },
    },
    ...
}
```

for more infos on the structure on the wasm-content check the next section.


#### Github pages

For the GitHub pages to work, the name of the repo must be specified in the config file. (name of app must match the name of the repo !!)

```ts
app: {
    baseURL: '/Wasm4Learn/',
    ...
}
,
```
