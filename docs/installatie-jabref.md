# JabRef

[JabRef](http://www.jabref.org/) is een gratis en open-source reference manager. Het is een Java applicatie die je kan gebruiken om de bibliografische gegevens van bronnen uit de wetenschappelijke of vakliteratuur te beheren.

JabRef is specifiek ontworpen voor LaTeX en gebruikt dan ook het standaard bestandsformaat voor bibliografische gegevens, nl. BibTeX/BibLaTeX (bestandsextensie .bib).

De interface en instellingen veranderen nogal eens tussen versies, dus het is mogelijk dat oudere screenshots niet meer overeen komen met de huidige versie en dat instructies niet meer exact werken.

## Installatie

We raden aan om een package manager te gebruiken voor de installatie van software, ook op Windows ([Winget](https://learn.microsoft.com/en-us/windows/package-manager/winget/)) of macOS ([Homebrew](https://brew.sh/)). Als je toch verkiest dat niet te doen, dan kan je het downloaden via de website: <https://www.jabref.org/#download>.

=== "Windows"

    ```console
    winget install JabRef.JabRef
    ```

=== "macOS"

    ```console
    brew install --cask jabref
    ```

=== "Debian/Ubuntu"

    ```console
    sudo apt install jabref
    ```

=== "RedHat/Fedora/SuSE"

    Ga naar <https://www.jabref.org/#download> en download het `.rpm` bestand. Installeer het vervolgens met:

    ```console
    sudo dnf install ./jabref*.rpm
    ```

    Of installeer via snap:

    ```console
    sudo snap install jabref
    ```

## Configuratie

Binnen de LaTeX-wereld is er een apart subsysteem voor het correct opmaken van een referentielijst of bibliografie. Het "oude" systeem heet BibTeX en is vaak de standaard in LaTeX-editors. Het sjabloon voor de paper en ook dat voor de bachelorproef zijn echter gebaseerd op een modernere vervanger, BibLaTeX/biber. Pas Jabref aan om standaard het laatste te gebruiken.

Open in het menu Options > Preferences en stel volgende instellingen in:

- General:
    - Default library mode: **biblatex**
- Entry Preview
    - Zorg er voor dat rechts onder "Selected" ook "American Psychological Association 7th edition" staat.
    - Andere geselecteerde stijlen kan je verwijderen (die hebben wij toch niet nodig), op "Custiomized preview Style" na.
- Linked Files
    - **File directory**, Main file directory: hier kan je het pad naar de *Main file directory* opgeven waar je alle PDF-versies van de artikels en andere bronnen bewaart.
        - Als je zorgt dat alle bestanden in deze directory dezelfde naam hebben als de Bibtex-key van de bron in je bibliografische databank (typisch naam van de eerste auteur + jaartal, bv. Knuth1998.pdf), dan kan JabRef dit automatisch terugvinden en kan je het openen vanuit JabRef zelf.
        - Tip: deze directory hoort in principe niet thuis in je Github-repository! 
