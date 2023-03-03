# JabRef

JabRef is een gratis en open-source reference manager. Het is een Java applicatie die je kan gebruiken om je bibliografische gegevens te beheren.

## Installatie

We raden aan om een package manager te gebruiken voor de installatie van software, ook op Windows ([Chocolatey](https://chocolatey.org)) of macOS ([Homebrew](https://brew.sh/)).

=== "Windows"

    ```console
    choco install jabref
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

    ```console
    sudo dnf install jabref
    ```

Als je toch verkiest dat niet te doen, dan kan je het downloaden via de website: <https://www.jabref.org/#download>.

## Configuratie

Open in het menu Options > Preferences en stel volgende instellingen in:

- General:
    - Default library mode: biblatex
- Entry Preview
    - Zorg er voor dat rechts onder "Selected" ook "American Psychological Association 7th edition" staat.
    - Andere geselecteerde stijlen kan je verwijderen (die hebben wij toch niet nodig), op "Custiomized preview Style" na.
- Linked Files
    - File directory, Main file directory: hier kan je het pad naar de directory opgeven waar je alle PDF-versies van de artikels en andere bronnen bewaart. Dit hoort trouwens niet in je Github-repository thuis! Als je zorgt dat alle bestanden in deze directory dezelfde naam hebben als de Bibtex-key van de bron in je bibliografische databank, dan kan JabRef dit terugvinden en kan je het openen vanuit JabRef zelf.
