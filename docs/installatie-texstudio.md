# TeXstudio

TeXstudio is een LaTeX-IDE die goed werkt op alle gangbare desktop-besturingssystemen. Dat is de reden waarom we deze meestal aanraden. Als je al gewend bent om [VS Code](installatie-vscode.md) te gebruiken, dan is dat echter ook een prima keuze!

## Installatie

We raden aan om een package manager te gebruiken voor de installatie van software, ook op Windows ([Winget](https://learn.microsoft.com/en-us/windows/package-manager/winget/)) of macOS ([Homebrew](https://brew.sh/)). Als je toch verkiest dat niet te doen, dan kan je het downloaden via de website: <https://www.texstudio.org/#download>.

=== "Windows"

    ```console
    winget install TeXstudio.TeXstudio
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

Oorspronkelijk kon LaTeX enkel om met ASCII-tekst, maar nu wordt ook Unicode (UTF-8) ondersteund. Dat vraagt wel enkele aanpassingen van de basisinstellingen.

Kies in het menu voor Options > Configure TeXstudio en pas volgende instellingen aan:

- **Build**:
    - Default compiler: **XeLaTeX** (UTF-8 compatibel, mogelijkheid om TTF-lettertypes te gebruiken, enz.) in plaats van PDFLaTeX (enkel ASCII, PostScript lettertypes, enz.)
    - Default Bibliography Tool: **Biber** (UTF-8 compatibel, ondersteuning voor APA-referenties, ...) in plaats van `bibtex` (enkel ASCII, geen APA-referenties, ...)
- **Commands**:
    - xelatex: `xelatex -shell-escape -synctex=1 -interaction=nonstopmode -file-line-error %` (voeg de optie `-shell-escape` toe)
- **Editor**:
    - Indentation mode: *Indent and Unindent Automatically*
    - Replace Indentation Tab by Spaces: *Aanvinken*
    - Replace Tab in Text by spaces: *Aanvinken*
    - Replace Double Quotes: *English Quotes: ‘‘’’*
- **Language Checking**:
    - Default language: selecteer "nl_NL-Dutch", "nl-BE" of een gelijkaardige optie voor Nederlands zodat je gebruik kan maken van spellingcontrole. Is deze optie toch niet beschikbaar? Je kan een woordenboekbestand voor OpenOffice of LibreOffice downloaden en installeren. Het dialoogvenster heeft links die je meteen naar de juiste pagina leiden.

## Algemeen gebruik

- Om een LaTeX-document (extensie .tex) te compileren, druk F5 (of kies in het menu voor Tools > Build & View)
    - De eerste keer dat je dit doet kan het compilatieproces lang duren. Er zal je op Windows wellicht gevraagd worden of MikTeX wijzigingen mag aanbrengen aan je systeem. Laat dit toe, want wellicht moeten er nog extra packages geïnstalleerd worden. Dit is eenmalig (per document), dus de volgende keer dat je compileert moet dit een stuk sneller gaan.
    - MiKTeX op Windows zal een pop-up tonen om je toestemming te vragen, bevestig dit. De eerste keer compileren kan enkele minuten duren zonder dat je feedback krijgt over wat er gebeurt. Even geduld, dus.
    - Op Linux werkt dit misschien niet en moet je opzoeken welke extra packages `texlive` je nog moet installeren voor de gewenste functionaliteit.
- Als je een document met een bibliografie wilt compileren, maar die is niet zichtbaar (en verwijzingen zijn in het vet gedrukt, bv. (**Knuth1977**)), dan moet je de bibliografie apart compileren met F8 (of Tools > Bibliography) en daarna opnieuw F5. Nu zou de bibliografie wel toegevoegd moeten zijn!

Indien er zich fouten voordoen bij de compilatie, kan je onderaan in het tabblad Log een overzicht krijgen van de foutboodschappen. LaTeX foutboodschappen interpreteren vraagt wel wat gewenning. De beste methode is om niet teveel code ineens te schrijven en vaak te compileren. Op die manier weet je dat de fout in je laatste toevoegingen moet zitten!

Wanneer je bij je lector hulp vraagt, is het belangrijk om de **exacte foutboodschap** mee te geven. Dat kan het makkelijkst door het tabblad *Logbestand* te selecteren en de gehele inhoud te kopiëren.
