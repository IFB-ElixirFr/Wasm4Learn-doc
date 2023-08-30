# Developpement of Wasm4Learn

## Project layout

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

!!! warning
    In public folder, webR files must be duplicated like content r folder

### Highlight on `nuxt.config.ts`

#### Nuxt content and GitHub

Configuring Nuxt content to fetch content from GitHub

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

#### Github pages

For the GitHub pages to work, the name of the repo must be specified in the config file.

```ts
app: {
    baseURL: '/Wasm4Learn/',
    ...
}
,
```


## Developpement

### Install dependencies

Make sure to install the dependencies:

```bash
yarn install
```

### Development Server

Start the development server on `http://localhost:3000`:

```bash

yarn dev
```

### Production

Build the application for production:

```bash
yarn deploy
```
