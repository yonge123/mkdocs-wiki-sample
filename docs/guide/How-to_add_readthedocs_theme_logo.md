# How to add logo in mkdocs

## 1. Edit readthedocs base.thml

- `/home/$USERNAME/anaconda3/envs/python37/lib/python3.7/site-packages/mkdocs/themes/readthedocs/base.html`

Replace 

```
<a href="{{ nav.homepage.url|url }}" class="icon icon-home"> {{ config.site_name }}</a>
```

With 

```
<a href="{{nav.homepage.url|url}}" class="icon icon-home"> {{ config.site_name }}
	<img src= "{{base_url}}/{{ config.theme.logo}}" class="logo" alt="logo"/>
</a>
```


## 2. add logo path in mkdocs.yml

- Logo Path: `docs/sources/images/logo.png`

```
site_name: 'Name'
theme: readthedocs
logo: 'sources/images/logo.png'

```


