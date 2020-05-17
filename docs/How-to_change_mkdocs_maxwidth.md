# How to change mkdocs maxwidth

- `/home/$USERNAME/anaconda3/envs/python37/lib/python3.7/site-packages/mkdocs/themes/readthedocs/css/theme.css`

Replace

```
.wy-nav-content {
    padding: 1.618em 3.236em;
    height: 100%;
    max-width: 800px;
    margin: auto
}
```

Width

```
.wy-nav-content {
    padding: 1.618em 3.236em;
    height: 100%;
    max-width: 1000px;
    margin: auto
}
```

