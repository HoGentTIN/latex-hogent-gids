# De HOGENT huisstijl

Zie de HOGENT-website voor officiële informatie over de huisstijl: <https://hogent.be/dit-is-hogent/huisstijl/>.

## Lettertypes

De HOGENT-huisstijl maakt gebruik van de lettertypes:

- Montserrat (Regular, Bold, ExtraBold, Black + Italic-versies van elk)
- Code Pro Black

Daarnaast gebruiken de LaTeX-sjablonen ook nog:

- Fira Code (monogespatieerd lettertype voor broncode, met ligaturen)
- Fira Math

Je kan de fonts downloaden vanuit de Github-repo voor de bachelorproef: <https://github.com/HoGentTIN/latex-hogent-bachproef/tree/main/fonts>.

Na downloaden kan je de lettertypes als volgt installeren:

=== "Windows"

    In bestandsbeheer Shift+rechtsklikken op het lettertypebestand (.otf) en kiezen voor "**Installeer voor alle gebruikers**"

    Je kan de bestanden ook kopiëren naar `C:\Windows\Fonts`

=== "macOS"

    In Finder dubbelklikken op het lettertypebestand (.otf) en in het preview-venster op de knop "Installeren" klikken.

    Je kan de bestanden ook kopiëren naar `/Library/Fonts` (systeembreed) of `~/Library/Fonts` (enkel voor huidige gebruiker).

=== "Debian/Ubuntu"

    In bestandsbeheer dubbelklikken op het lettertypebestand (.otf) en in het preview-venster op de knop "Installeren" klikken.

    Je kan de bestanden ook kopiëren naar `/usr/share/fonts` (systeembreed) of `~/.local/share/fonts` (enkel voor huidige gebruiker).

## Sjablonen in de HOGENT huisstijl

Volgende LaTeX-sjablonen zijn conform met de huisstijlregels (of pogen dat in elk geval te doen). Let wel, deze zijn niet officieel erkend door de dienst communicatie.

- [latex-hogent-article](https://github.com/HoGentTIN/latex-hogent-article): sjabloon voor korte documenten zoals een artikel, opgave, ...
- [latex-hogent-report](https://github.com/HoGentTIN/latex-hogent-report): sjabloon voor langere documenten zoals een stageverslag, syllabus, cursus, ...
- [latex-hogent-bachproef](https://github.com/HoGentTIN/latex-hogent-bachproef): sjabloon voor de bachelorproef toegepaste informatica
    - Gebaseerd op latex-hogent-report (scriptie) en latex-hogent-article (onderzoeksvoorstel)
- [latex-hogent-beamer](https://github.com/HoGentTIN/latex-hogent-beamer): Beamer-presentatie
- [latex-hogent-exam](https://github.com/HoGentTIN/latex-hogent-exam): sjabloon voor examenopgave + modeloplossing

## Huisstijlkleuren

De HOGENT-huisstijl maakt gebruik een aantal specifieke kleuren. In de sjablonen zijn deze ook gedefinieerd als kleurvariabelen. Hieronder vind je een overzicht van de kleuren, de naam waaronder je ze kan gebruiken in LaTeX-documenten, en hun RGB-/HEX-waarden.

| RGB         | HEX     | Naam              | Voorbeeld                                           |
| :---------- | :------ | :---------------- | :-------------------------------------------------- |
| 22,176,165  | #16B0A5 | hogent-darkgreen  | <div style="background-color: #16B0A5">&nbsp;</div> |
| 76,162,213  | #4CA2D5 | hogent-blue       | <div style="background-color: #4CA2D5">&nbsp;</div> |
| 165,202,114 | #A5CA72 | hogent-lightgreen | <div style="background-color: #A5CA72">&nbsp;</div> |
| 187,144,189 | #BB90BD | hogent-purple     | <div style="background-color: #BB90BD">&nbsp;</div> |
| 195,187,175 | #C3BBAF | hogent-grey       | <div style="background-color: #C3BBAF">&nbsp;</div> |
| 216,176,131 | #D8B083 | hogent-brown      | <div style="background-color: #D8B083">&nbsp;</div> |
| 239,135,103 | #EF8767 | hogent-orange     | <div style="background-color: #EF8767">&nbsp;</div> |
| 241,157,160 | #F19DA0 | hogent-pink       | <div style="background-color: #F19DA0">&nbsp;</div> |
| 244,222,0   | #F4DE00 | hogent-yellow     | <div style="background-color: #F4DE00">&nbsp;</div> |
| 250,188,50  | #FABC32 | hogent-ochre      | <div style="background-color: #FABC32">&nbsp;</div> |