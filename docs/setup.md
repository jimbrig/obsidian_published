# Setup ⚙️

## MkDocs

```powershell
pip install mkdocs
mkdocs build
mkdocs serve
mkdocs gh-deploy
```

## Plugins

|                  Plugin                   | Version |
| :---------------------------------------: | :-----: |
|                  mkdocs                   |  1.1.2  |
|          mkdocs-autolinks-plugin          |  0.4.0  |
|        mkdocs-awesome-pages-plugin        |  2.5.0  |
| mkdocs-git-revision-date-localized-plugin |  0.9.2  |
|           mkdocs-minify-plugin            |  0.4.0  |
|          mkdocs-monorepo-plugin           | 0.4.14  |
|          mkdocs-roamlinks-plugin          |  0.1.3  |

## Installations

```powershell
$ pip install mkdocs /
    mkdocs-autolinks-plugin /
    mkdocs-awesome-pages-plugin /
    mkdocs-git-revision-date-localized-plugin /
    mkdocs-monorepo-plugin /
    mkdocs-roamlinks-plugin /
    mkdocs-minify-plugin

$ pip list | grep mkdocs-*
mkdocs                                    1.1.2
mkdocs-autolinks-plugin                   0.4.0
mkdocs-awesome-pages-plugin               2.5.0
mkdocs-git-revision-date-localized-plugin 0.9.2
mkdocs-minify-plugin                      0.4.0
mkdocs-monorepo-plugin                    0.4.14
mkdocs-roamlinks-plugin                   0.1.3
```

### Configuration

```yaml
plugins:
  - search
  - autolinks
  - roamlinks
  - awesome-pages
  - git-revision-date-localized:
      type: timeago
  - minify:
      minify_html: true
markdown_extensions:
  - toc:
      permalink: ⚑
      baselevel: 2
  - codehilite:
      linenums: false
      guess_lang: true
  - footnotes
  - abbr
  - admonition
  - meta
  - def_list
```