# Welcome to MkDocs

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Install MKDocs

```
pip install mkdocs
pip install mkdocs-material
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



<br>

## MKDocs Offline Site 

Mkdocs 를 Build 후 Intranet 에서 사용시  Site 폴더 아래 모든 html 파일을 아래 처럼 변경 해야 html 실행 시 지연 없이 바로 볼수 있습니다. 

이 작업을 하지 않을 경우 방화벽 까지 가서 접속인 않되는 것을 확 인 하기때문에 시간이 오래 걸립니다.

인터넷이 연결 되어있을경우 크게 상관은 없습니다.


```
Replace 
<link href="https://fonts.gstatic.com" rel="preconnect" crossorigin>

With
<!-- <link href="https://fonts.gstatic.com" rel="preconnect" crossorigin> -->

Replace
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Roboto:300,400,400i,700%7CRoboto+Mono&display=fallback">

With
<!-- <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Roboto:300,400,400i,700%7CRoboto+Mono&display=fallback"> -->
```
