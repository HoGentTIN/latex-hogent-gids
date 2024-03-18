# Vaak voorkomende problemen

## Font niet gevonden

![Error message: font cannot be found.](images/error-font-cannot-be-found.png)

Als je in de foutboodschap een van de volgende fonts ziet: Montserrat, Fira Code, Fira Math, Code Pro Black, dan heb je de lettertypes die bij de HOGENT-huisstijl horen nog niet (correct) geïnstalleerd. Zie [Lettertypes](hogent-huisstijl.md#lettertypes) voor instructies.

## Ontbrekende packages

Als je bij compilatie in TeXStudio of VSCode op Windows het volgende ziet:

![MikTeX: ontbrekende packages installeren.](images/miktex-06.png)

klik dan onderaan "Always show dis dialog" UIT en klik op "Install". Zie ook [MikTeX installatie](installatie-miktex.md#installatie-van-ontbrekende-packages).

Als je de foutboodschap ziet in het Messages-paneel onderaan, bv.:

```plaintext
! LaTeX Error: File `lipsum.sty' not found.
```

dan is er ofwel iets misgelopen bij de installatie, ofwel heb je MikTeX niet toegelaten packages automatisch te installeren. Open de MikTeX Console, ga naar "Packages", zoek de ontbrekende package in de lijst en klik op de installeerknop (plus-icoon).

![MikTeX Console: Package manueel installeren](images/miktex-08.png)

Je kan MikTeX instellen dat packages automatisch geïnstalleerd worden. Zie [MikTeX installatie](installatie-miktex.md#installatie-van-ontbrekende-packages).
