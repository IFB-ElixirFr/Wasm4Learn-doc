# Developpement of Wasm4Learn content


## Project layout

```bash
...
/content
    /language                                       # the programming languages implemented
        /R                                          # Langage name 
            /tutorials
                /1.tuto
                    _dir.yml
                    1.tuto_content.md
                    2.tuto_content.md
                    ...
                2.tuto/
                ...
            /classes
                /images                             # images used in the classes
                1.class.md
                2.class.md
                ...
            _dir.yaml                               # Metadata for language
        /js
            ...
        /python
            ...
    /learning-path
        /1.formation-language          
            _dir.yml                                    # Metadata for the learning path
            1.tuto_content.md
            ... 
        ...
    /tool                                           # other implemented tools     
        /gawk
            _dir.yml                                # Metadata for the tool
            /tutorials
                /1.tuto_tool
                    _dir.yml
                    1.tuto_tool_content.md
                    2.tuto_tool_content.md
        /grep
            ...
        ...

```

### Example of ```_dir.yml``` file for language

```yaml
title: 'R'
navigation.description : "R is a language and environment for statistical computing and graphics."
navigation.image: "https://cran.r-project.org/Rlogo.svg"
```

### Example of ```_dir.yml``` file for section

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