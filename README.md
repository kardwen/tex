# My TeX setup

Documentation for my TeX setup, results may vary

## TeX editor

Visual Studio Code with the LaTeX-Workshop ([GitHub repository](https://github.com/James-Yu/LaTeX-Workshop)) extension works pretty well and lets you set up version control.
Additionally, you can install the [LTeX](https://github.com/valentjn/vscode-ltex) extension for spell checking.

VS Code extensions:

* [LaTeX-Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)
* [LTeX](https://marketplace.visualstudio.com/items?itemName=valentjn.vscode-ltex)

## TeX distribution

The LaTeX-Workshop [installation instructions](https://github.com/James-Yu/LaTeX-Workshop/wiki/Install#installation-and-basic-settings) recommend installing TeXLive as the TeX distribution. I opted for [TinyTeX](https://yihui.org/tinytex) instead, which is faster to install and takes up less space, but has the disadvantage that packages have to be installed manually.

### TinyTeX

Follow the [installation notes](https://yihui.org/tinytex/#installation) for TinyTeX, binary packages are available on [GitHub](https://github.com/rstudio/tinytex-releases/releases).

Install additional packages by typing ``tlmgr install <pkgname>`` in your terminal emulator, below are the commands for the packages I have installed:

```sh
tlmgr update --self

tlmgr install babel-english
tlmgr install babel-german
tlmgr install hyphen-german
tlmgr install csquotes
tlmgr install biblatex
tlmgr install biblatex-ieee
tlmgr install biber
tlmgr install fancyhdr
```

For BibLaTeX, ``biber`` may have to be installed and added to PATH, e.g. in ``~/.bashrc``:

```sh
export PATH=$PATH:~/.TinyTeX/bin/x86_64-linux
```

## Templates

You can find a simple example of an article in the ``templates`` directory.
