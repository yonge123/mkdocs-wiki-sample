# Welcome to MkDocs

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Install MKDocs

```
pip install mkdocs
pip install pymdownx
pip install pyembed

```


## Commands
* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.


Sample

```
# create project folder
mkdir mkdocs_test
cd mkdocs_test

# create new mkdocs project in this directory
mkdocs new .

# site/ -> gitignore
echo "site/" >> .gitignore

# start serve
mkdocs serve

# build Site
mkdocs build



# push to github gh-pages
mkdocs gh-deploy




# push to gitlab ci  

- reference: https://gitlab.com/pages/mkdocs/commit/48f7b16f3d1ce0bf4b8fd30b29b3ef94b77e496d
- create .gitlab-ci.yml file 

image: python:3.8-buster

before_script:
  - pip install mkdocs
  ## Add your custom theme if not inside a theme_dir
  ## (https://github.com/mkdocs/mkdocs/wiki/MkDocs-Themes)
  # - pip install mkdocs-material

pages:
  script:
  - mkdocs build
  - mv site public
  artifacts:
    paths:
    - public
  only:
  - master

```

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.


## MKDocs Extension

- [https://python-markdown.github.io/extensions/](https://python-markdown.github.io/extensions/)
- [https://facelessuser.github.io/pymdown-extensions/](https://facelessuser.github.io/pymdown-extensions/)
- [https://github.com/Python-Markdown/markdown/wiki/Third-Party-Extensions](https://github.com/Python-Markdown/markdown/wiki/Third-Party-Extensions)
- [https://github.com/pyembed/pyembed-markdown](https://github.com/pyembed/pyembed-markdown)
- [https://github.com/mkdocs/mkdocs/wiki/MkDocs-Plugins](https://github.com/mkdocs/mkdocs/wiki/MkDocs-Plugins)


## MKDocs Plugin

- https://www.mkdocs.org/user-guide/plugins/#developing-plugins

