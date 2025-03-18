# Wat te doen bij problemen?

Wanneer het compileren van een LaTeX-document niet lukt, kan dat verschillende oorzaken hebben. Zeker bij het opzetten van je werkomgeving kan het gebeuren dat een en ander niet van de eerste keer werkt.

## Checklist

Hieronder vind je enkele zaken die je in elk geval eerst kan proberen voordat je verder hulp zoekt.

- Controleer of je de LaTeX-distributie hebt geïnstalleerd en of de laatste updates geïnstalleerd zijn. In MikTeX op Windows kan je dit controleren via de MikTeX-console (zie [MikTeX installatie](installatie-miktex.md#eerste-gebruik-updates-installeren)). Op macOS of Linux gebruik je je package manager om de laatste updates te installeren.

- Controleer of je editor of IDE correct geconfigureerd is, in het bijzonder of je de juiste compilers en opties gebruikt. Zie [TeXStudio](installatie-texstudio.md#configuratie) of [VSCode](installatie-vscode.md#configuratie) voor meer info.

- Controleer of de fonts voor de HOGENT-huisstijl geïnstalleerd zijn. Zie [Lettertypes](hogent-huisstijl.md#lettertypes) voor instructies.

- Ga in het .log-bestand op zoek naar de foutboodschap en probeer die te begrijpen en eventueel op te zoeken op het internet, of specifiek op [tex.stackexchange.com](https://tex.stackexchange.com). Jammer genoeg zijn de foutboodschappen van LaTeX niet altijd even duidelijk, en soms zetten ze je zelfs op het verkeerde spoor.

- Kijk eens op de pagina met [vaak voorkomende problemen](problemen.md) of jouw specifieke probleem al niet vermeld staat.

## Hulp vragen

Als je hulp vraagt bij een van de lectoren, voorzie dan zeker de volgende informatie:

- Het .log-bestand in dezelfde directory als het .tex-bestand bevat de volledige uitvoer van de compiler met alle foutboodschappen. Dit bestand is cruciaal om te weten wat er fout loopt.

- Je kan best toegang geven tot je Github-repository met de LaTeX-broncode, ofwel deze doorsturen in een .zip-bestand. Zo kunnen we proberen om je probleem te reproduceren en helpen om het op te lossen.

