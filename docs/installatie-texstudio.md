# TeXstudio

TeXstudio is een LaTeX-IDE die goed werkt op alle gangbare desktop-besturingssystemen. Dat is de reden waarom we deze meestal aanraden. Als je al gewend bent om [VS Code](installatie-vscode.md) te gebruiken, dan is dat echter ook een prima keuze!

## Installatie

We raden aan om een package manager te gebruiken voor de installatie van software, ook op Windows ([Chocolatey](https://chocolatey.org)) of macOS ([Homebrew](https://brew.sh/)). Als je toch verkiest dat niet te doen, dan kan je het downloaden via de website: <https://www.texstudio.org/#download>.

=== "Windows"

    ```console
    choco install texstudio
    ```

=== "macOS"

    ```console
    brew install --cask texstudio
    ```

=== "Debian/Ubuntu"

    ```console
    sudo apt install texstudio
    ```

=== "Fedora"

    ```console
    sudo dnf install texstudio
    ```

## Configuratie

Kies in het menu voor Options > Configure TeXstudio en pas volgende instellingen aan:

- Build:
    - Default compiler: "XeLaTeX"
    - Default Bibliography Tool: "Biber"
- Commands:
    - xelatex: `xelatex -shell-escape -synctex=1 -interaction=nonstopmode -file-line-error %`
- Editor:
    - Indentation mode: Indent and Unindent Automatically
    - Replace Indentation Tab by Spaces: Aanvinken
    - Replace Tab in Text by spaces: Aanvinken
    - Replace Double Quotes: English Quotes: ‘‘’’
- Language Checking:
    – Default language: selecteer "nl_NL-Dutch", "nl-BE" of een gelijkaardige optie voor Nederlands zodat je gebruik kan maken van spellingcontrole. Is deze optie toch niet beschikbaar? Je kan een woordenboekbestand voor OpenOffice of LibreOffice downloaden en installeren. Het dialoogvenster heeft links die je meteen naar de juiste pagina leiden.

## Gebruik

- Om een LaTeX-document (extensie .tex) te compileren, druk F5 (of kies in het menu voor Tools > Build & View)
- Als je een document met een bibliografie wilt compileren, maar die is niet zichtbaar (en verwijzingen zijn in het vet gedrukt, bv. (**Knuth1977**)), dan moet je de bibliografie apart compileren met F8 (of Tools > Bibliography) en daarna opnieuw F5.
