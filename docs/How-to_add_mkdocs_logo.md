# How to add logo in mkdocs

## 1. Edit readthedocs base.thml

- `/home/$USERNAME/anaconda3/envs/python37/lib/python3.7/site-packages/mkdocs/themes/readthedocs/base.html`

Replace 

```
<a href="{{ nav.homepage.url|url }}" class="icon icon-home"> {{ config.site_name }}</a>
```

With 

```
<a href="{{ nav.homepage.url|url }}" class="icon icon-home"> {{ config.site_name }}
	<img src= "{{ config.logo }}" class="logo" alt="Logo"/>
</a>
```


## 2. add logo path in mkdocs.yml

```
site_name: 'Name'
theme: readthedocs
logo: 'sources/images/logo.png'

```

## 3. 

- logo 경로 는 항상 고정되어 있어서 md 파일 이 다른 폴더 안에 들어 있으면 logo 의 상대경 로가 변경 되므로 logo 가 나타나지 않는 문제가 있습니다.

logo 정상출력 하려면 아래와 같은 구조 을 가져야 합니다.

```
# logo
docs/sources/images/logo.png

# md 
docs/file.md

# setting
mkdocs.yml
	logo: sources/images/logo.png

```

아래와 같이 file.md 가 docs/folder 아래 있을경우 logo 이 상대 경로 가 변경 되어 logo 가 나타나지 않습니다. 

```
# logo
docs/sources/images/logo.png

# md 
docs/folder/file.md

# setting
mkdocs.yml
	logo: sources/images/logo.png

```
