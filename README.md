# Published Vault

[![Publish Vault](https://github.com/jimbrig/obsidian_published/actions/workflows/publish.yml/badge.svg)](https://github.com/jimbrig/obsidian_published/actions/workflows/publish.yml)
## Setup

### MkDocs

```powershell
pip install mkdocs
mkdocs build
mkdocs serve
mkdocs gh-deploy
```

### Plugins

|                  Plugin                   | Version |
| :---------------------------------------: | :-----: |
|                  mkdocs                   |  1.1.2  |
|          mkdocs-autolinks-plugin          |  0.4.0  |
|        mkdocs-awesome-pages-plugin        |  2.5.0  |
| mkdocs-git-revision-date-localized-plugin |  0.9.2  |
|           mkdocs-minify-plugin            |  0.4.0  |
|          mkdocs-monorepo-plugin           | 0.4.14  |
|          mkdocs-roamlinks-plugin          |  0.1.3  |

#### Installations

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

#### Configuration

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

### Apendix: Publish Obsidian Notes with MkDocs (template)

Would you like to make some of your [Obsidian](https://obsidian.md/) notes public?

This template gives you an easy way to publish your Obsidian notes using Github pages.

With this template, you get these out-of-the-box:

- an awesome website based on Material theme, complete with a search bar (Checkout this template published [here](https://jobindj.github.io/obsidian-mkdocs/))
- get the Obsidian/Roam style `[[wikilinks]]` from your vault in your published notes
- Toggle between light and dark mode

#### How to get started?

1. Create a new github repository using [this template](https://github.com/jobindj/obsidian-mkdocs/generate)
    - Give a name to your public notes repository in this step. By default your notes will be published at `<https://username.github.io/repo-name/>`
    - You need to copy only the `main` branch while create the repo from the template
2. Clone the repository you generated into your Obsidian folder/vault.
3. Move the notes you would like to make public to the `repo-name/docs` folder.
    - Easiest way to do this would be using drag and drop within Obsidian
4. Commit and push the changes. Github actions will publish your notes using [MkDocs](https://www.mkdocs.org/), with the [Material theme](https://squidfunk.github.io/mkdocs-material/).

#### Configuring your website

#### How do I arrange sections and pages?

By default, the sections and pages will follow the folder structure within `/docs`.

- If you would like to arrange the pages manually, then use the `nav` option in the `mkdocs.yml` [configuration file](https://www.mkdocs.org/#adding-pages) at the root of this repo  to set custom page navigation.
  - For example, see the setup for [the Blue Book](https://lyz-code.github.io/blue-book/) at [github](https://github.com/lyz-code/blue-book/blob/master/mkdocs.yml). Managing each page using `nav` can become cumbersome as the number of notes increase though!
- The Materials theme provides multiple options to arrange [sections](https://squidfunk.github.io/mkdocs-material/setup/setting-up-navigation/#navigation-sections), use [navigation tabs](https://squidfunk.github.io/mkdocs-material/setup/setting-up-navigation/#navigation-tabs), and many other helpful [navigation setups](https://squidfunk.github.io/mkdocs-material/setup/setting-up-navigation/)

#### Alternatives

- [kmaasrud/oboe](https://github.com/kmaasrud/oboe): tool to convert an Obsidian vault into a static directory of HTML files.
- [Jackiexiao/foam-mkdocs-template](https://github.com/Jackiexiao/foam-mkdocs-template): template for Obsidian/Foam using mkdocs/mkdocs-material/mkdocs-roamlinks-plugin
- [foambubble/foam-template](https://github.com/foambubble/foam-template): Foam workpace template
