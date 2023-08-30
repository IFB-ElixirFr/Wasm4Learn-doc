# Developpement of Wasm4Learn content


## Project layout

```bash
...
/content
    /language               # the programming languages implemented
        /R                  # Langage name 
            /tutorials
                ...
            /classes
            _dir.yaml       # Metadata for language     

        /js
            ...
        /python
            ...
        /ruby
            ...
    /learning-path          # function shared in all project
        ...             
    /tool              
        /gawk
            ...
        /grep
            ...
        /sed
            ...

```

### Example of _dir.yml file for language

```yaml
title: 'R'
navigation.description : "R is a language and environment for statistical computing and graphics."
navigation.image: "https://cran.r-project.org/Rlogo.svg"
```

### Example of _dir.yml file for section

```yaml
title: 'Les premiers pas en R'
navigation.description : "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed non risus. Suspendisse lectus tortor, dignissim sit amet, adipiscing nec, ultricies sed, dolor. "
navigation.belt:
  - "white"
navigation.tags:
  - "R"
  - "console"
```


## Write content

Pages are written in MarkDown. A number of components have been added to enrich the development platform, and are described in detail in the following section.

Once the content has been written according to the project structure above, all that's left to do is upload the changes to GitHub.