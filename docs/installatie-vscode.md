# Visual Studio Code

VS Code is een veelzijdige teksteditor met zeer goede ondersteuning voor tientallen programmeer- en scriptingtalen en gestructureerde tekstformaten als HTML, Markdown, enz. Ook voor LaTeX zijn er goede plugins. Als je al gewend bent om VS Code te gebruiken, dan kan je het even goed ook gebruiken voor LaTeX. Het nadeel is misschien wel dat het wat complexer is om Code goed te configureren.

## Installatie

We raden aan om een package manager te gebruiken voor de installatie van software, ook op Windows ([Winget](https://learn.microsoft.com/en-us/windows/package-manager/winget/)) of macOS ([Homebrew](https://brew.sh/)). Als je toch verkiest dat niet te doen, dan kan je het downloaden via de website: <https://code.visualstudio.com/download>.

=== "Windows"

    ```console
    winget install Microsoft.VisualStudioCode
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

Plak de inhoud van het codeblok hieronder (zonder de buitenste accolades) onderaan de User Settings (JSON) in Visual Studio Code. Typ Ctrl+Shift+P in om het "command palette" te openen, en zoek "Preferences: open user settings (JSON)".

```json
{
  "latex-workshop.latex.recipes": [
        {
            "name": "xelatex× 2",
            "tools": [
                "xelatex",
                "xelatex"
            ]
        },
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
            "name": "latexmk 🔃",
            "tools": [
                "latexmk"
            ]
        }
    ],
    "latex-workshop.latex.tools": [
        {
            "args": [
                "-f",
                "-xelatex",
                "-shell-escape",
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "-outdir=%OUTDIR%",
                "%DOC%"
            ],
            "command": "latexmk",
            "env": {},
            "name": "latexmk"
        },
        {
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-shell-escape",
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
    "latex-workshop.latex.clean.method": "glob",
    "latex-workshop.latex.clean.fileTypes": [
        "**/*.acn",
        "**/*.acr",
        "**/*.alg",
        "**/*.aux",
        "**/*.bbl",
        "**/*.bcf",
        "**/*.bib.bak",
        "**/*.blg",
        "**/*.dvi",
        "**/*.fdb_latexmk",
        "**/*.fls",
        "**/*.glg",
        "**/*.glo",
        "**/*.gls",
        "**/*.glsdefs",
        "**/*.idx",
        "**/*.ind",
        "**/*.ist",
        "**/*.lof",
        "**/*.lol",
        "**/*.lop",
        "**/*.lot",
        "**/*.nav",
        "**/*.out",
        "**/*.run.xml",
        "**/*.snm",
        "**/*.synctex",
        "**/*.synctex(busy)",
        "**/*.synctex.gz",
        "**/*.synctex.gz(busy)",
        "**/*.tdo",
        "**/*.toc",
        "**/*.xdv",
        "**/_minted-main",
        "**/_minted-main/*"
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
    ],
}
```

## Meer info

- Maithripala, A. (2020) *How to create and compile LateX documents on Visual Studio Code.* Opgehaald 2024-02-10 van <https://dev.to/ucscmozilla/how-to-create-and-compile-latex-documents-on-visual-studio-code-3jbk>.
- Van Vreckem, B. (2023) *Visual Studio Code settings - settings.json.* Opgehaald 2024-02-10 van <https://github.com/bertvv/dotfiles/blob/main/.config/Code/User/settings.json>
