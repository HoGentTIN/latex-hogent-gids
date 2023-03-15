# Visual Studio Code

VS Code is een veelzijdige editor met ondersteuning voor allerlei documenttypen, waaronder LaTeX.

## Installatie

We raden aan om een package manager te gebruiken voor de installatie van software, ook op Windows ([Chocolatey](https://chocolatey.org)) of macOS ([Homebrew](https://brew.sh/)). Als je toch verkiest dat niet te doen, dan kan je het downloaden via de website: <https://code.visualstudio.com/download>.

=== "Windows"

    ```console
    choco install vscode
    ```

=== "macOS"

    ```console
    brew install --cask visual-studio-code
    ```

=== "Debian/Ubuntu"

    Ga naar <https://code.visualstudio.com/download> en download de .deb-versie. Open een terminal in de directory met de .deb en voer het volgende commando uit:

    ```console
    sudo apt install ./code_*.deb
    ```

=== "RedHat/Fedora/SuSE"

    Ga naar <https://code.visualstudio.com/download> en download de .rpm-versie. Open een terminal in de directory met de .deb en voer het volgende commando uit:


    ```console
    sudo dnf install ./code-*.rpm
    ```

## Configuratie

Installeer eerst en vooral de [LaTeX Workshop-extensie](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) van James-Yu.

Plak de inhoud van dit bestand (zonder accolades) onderaan de User Settings (JSON) in Visual Studio Code. Je vindt de user settings door via F1 te zoeken naar "user settings".

```json
{
  "latex-workshop.latex.recipes": [
    {
        "name": "xelatex ➞ biber ➞ xelatex× 2",
        "tools": [
            "xelatex",
            "biber",
            "xelatex",
            "xelatex"
        ]
    },
    {
        "name": "xelatex× 2",
        "tools": [
            "xelatex",
            "xelatex"
        ]
    }
  ],
  "latex-workshop.latex.tools": [
      {
          "args": [
              "-synctex=1",
              "-interaction=nonstopmode",
              "--shell-escape",
              "-file-line-error",
              "%DOC%"
          ],
          "command": "xelatex",
          "env": {},
          "name": "xelatex"
      },
      {
          "args": [
              "%DOCFILE%"
          ],
          "command": "bibtex",
          "env": {},
          "name": "bibtex"
      },
      {
          "args": [
              "%DOCFILE%"
          ],
          "command": "biber",
          "env": {},
          "name": "biber"
      }
  ],
  "latex-workshop.view.pdf.viewer": "tab",
  "latex-workshop.latex.autoBuild.run": "onSave",
  "latex-workshop.latex.recipe.default": "first",
  "latex-workshop.latex.autoClean.run": "onBuilt",
  "latex-workshop.latex.clean.fileTypes": [
      "*.acn",
      "*.acr",
      "*.alg",
      "*.aux",
      "*.bbl",
      "*.bcf",
      "*.bib.bak",
      "*.blg",
      "*.dvi",
      "*.fdb_latexmk",
      "*.fls",
      "*.glg",
      "*.glo",
      "*.gls",
      "*.glsdefs",
      "*.idx",
      "*.ind",
      "*.ist",
      "*.lof",
      "*.lol",
      "*.lop",
      "*.lot",
      "*.nav",
      "*.out",
      "*.run.xml",
      "*.snm",
      "*.synctex",
      "*.synctex(busy)",
      "*.synctex.gz",
      "*.synctex.gz(busy)",
      "*.tdo",
      "*.toc",
      "*.vrb",
      "*.xdv",
      "_minted-*/"
  ],
  "latex-workshop.bibtex-format.sort.enabled": true,
  "latex-workshop.intellisense.citation.backend": "biblatex",
  "latex-workshop.intellisense.package.enabled": true,
  "latex-workshop.latex.autoBuild.cleanAndRetry.enabled": false,
  "latex-workshop.latex.autoBuild.interval": 30000,
  "latex-workshop.latex.clean.subfolder.enabled": true,
  "latex-workshop.latex.magic.args": [
      "-synctex=1",
      "-interaction=nonstopmode",
      "-file-line-error",
      "--shell-escape",
      "%DOC%"
  ]
}
```
