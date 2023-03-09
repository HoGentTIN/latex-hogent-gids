# TeX live

[TeX live](https://tug.org/texlive/) is tegenwoordig de standaard LaTeX-distributie voor de meeste Linux-distributies en kan ook op Windows geïnstalleerd worden.

## Installatie

Op Linux zijn de te installeren packages in principe beschikbaar via de repositories van de distributie die je gebruikt. Texlive is typisch onderverdeeld in honderden individuele packages, maar je kan ook een selectie van de meest gebruikte installeren zodat je niet de volledige distributie (al gauw meerdere GBs) moet binnen halen. Daarvoor heeft men "collection" packages gecreëerd die zelf geen inhoud hebben, maar de andere packages als dependency binnenhalen. We geven hieronder CLI-instructies voor Ubuntu/Debian en voor Fedora. Pas zelf aan waar nodig, en het is ook best mogelijk dat je achteraf nog extra zaken zal moeten installeren.

=== "Windows"

    ```console
    choco install texlive --params="'/collections:xetex'"
    ```

=== "Debian/Ubuntu"

    ```console
    sudo apt install texlive-base texlive-latex-base texlive-latex-recommended texlive-bibtex-extra texlive-pictures texlive-fonts-recommended
    ```

=== "RedHat/Fedora/SuSE"

    ```console
    sudo dnf install texlive-collection-latex texlive-babel-dutch
    ```
