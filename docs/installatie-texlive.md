# TeX live

[TeX live](https://tug.org/texlive/) is tegenwoordig de standaard LaTeX-distributie voor de meeste Linux-distributies en kan ook op Windows geïnstalleerd worden.

## Installatie

Op Linux zijn de te installeren packages in principe beschikbaar via de repositories van de distributie die je gebruikt. Texlive is typisch onderverdeeld in honderden individuele packages, maar je kan ook een selectie van de meest gebruikte installeren zodat je niet de volledige distributie (al gauw meerdere GBs) moet binnen halen. Daarvoor heeft men "collection" packages gecreëerd die zelf geen inhoud hebben, maar de andere packages als dependency binnenhalen. We geven hieronder CLI-instructies voor Ubuntu/Debian en voor Fedora. Pas zelf aan waar nodig, en het is ook best mogelijk dat je achteraf nog extra zaken zal moeten installeren.

=== "Windows"

    Volg de instructies op <https://www.tug.org/texlive/windows.html>
    
    - Download de [installer van de website](https://mirror.ctan.org/systems/texlive/tlnet/install-tl-windows.exe)
    - Start deze op als Administrator en kies voor "Install"
    - Onder "Geavanceerd" kan je in detail bepalen welke LaTeX packages je al dan niet installeert. Als je voldoende vrije schijfruimte hebt (8 a 9 GB), kan je ook gewoon alles installeren. De TeXworks frontend hoef je niet te installeren, voor deze cursus heb je die niet nodig.

=== "Debian/Ubuntu"

    ```console
    sudo apt install biber texlive-extra-utils texlive-fonts-recommended texlive-lang-european texlive-latex-base texlive-latex-extra texlive-latex-recommended texlive-pictures texlive-xetex python3-pygments latexmk
    ```

=== "RedHat/Fedora/SuSE"

    ```console
    sudo dnf install texlive-collection-latex texlive-babel-dutch
    ```

## Gebruik onder Windows

- Je kan een lijst van geïnstalleerde en beschikbare pakketten bekijken en beheren via de *TeX Live Shell*. Deze moet met Administrator-rechten draaien, dus je krijgt bij opstarten de vraag of de app wijzigingen mag aanbrengen aan je systeem. Dit is nodig om de packages te installeren vanaf een CTAN (Comprehensive TeX Archive Network) repository.
  - In het menu Opties > Informatiebronnen... kan je een CTAN mirror kiezen die dicht bij je locatie ligt.
- Je kan een package installeren in een Administrator-terminal met `tlmgr install <package>`.
