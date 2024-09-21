# Welcome

Welcome to test-mkdocs.

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.
* `mkdocs gh-deploy` - Deploy your documentation to GitHub Pages.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

We will mainly see and modify ``./mkdocs.yml`` file and ``./docs/`` directory.

# Customize MKDocs Theme

Please visit [Lantana](https://lantana.wsoft.ws/) for more information.

## Install theme
    pip install lantana

## Modify mkdocs.yml

```yml title="mkdocs.yml"
site_name: Tech Note

docs_dir : 'docs'

extra_javascript:
  - https://polyfill.io/v3/polyfill.min.js?features=es6
  - https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js

language : ja


theme: lantana

visible_search : true

plugins:
    - search:
        lang : 'ja'
        min_search_length: 2
    - macros
    - awesome-pages
    - git-authors

markdown_extensions:
    - attr_list
    - pymdownx.highlight:
       anchor_linenums: true
    - admonition
    - pymdownx.arithmatex:
       generic : true
    - md_in_html
    - pymdownx.details
    - pymdownx.superfences:
        custom_fences:
          - name: mermaid
            class: mermaid
            format: !!python/name:pymdownx.superfences.fence_code_format
    - lantana.mermaid_precompile
    - lantana.codeblock_copybtn
    - pymdownx.snippets
    - pymdownx.critic
    - pymdownx.caret
    - pymdownx.keys
    - pymdownx.mark
    - pymdownx.tilde
    - pymdownx.emoji:
        emoji_index: !!python/name:materialx.emoji.twemoji
        emoji_generator: !!python/name:materialx.emoji.to_svg
    - pymdownx.tasklist:
        custom_checkbox: true
    - pymdownx.magiclink
    - pymdownx.striphtml
```

## Example mermaid

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

