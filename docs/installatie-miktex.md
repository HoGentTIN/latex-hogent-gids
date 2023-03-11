# MikTeX

[MikTeX](https://miktex.org) is wellicht de oudste en bekendste LaTeX-distributie voor Windows. MikTeX heeft een ingebouwde package manager die automatisch ontbrekende packages installeert. Op die manier kan de initiële installatie relatief klein gehouden worden.

## Installatie

We raden aan om een package manager te gebruiken om software te installeren op Windows ([Chocolatey](https://chocolatey.org/)). Indien je dit toch niet wenst te doen, dan kan je het downloaden via de website: <https://miktex.org/download>.

```console
choco install miktex
```

## Configuratie

Na installatie is het belangrijk om de [MikTeX-console](https://miktex.org/howto/miktex-console) te openen en de instructies daar te volgen. Je krijgt een melding dat er nog niet gecontroleerd is op updates. Als je dit niet doet, dan zal het compileren van een LaTeX-document ook niet lukken.

Klik "Switch to MiKTeX administrator mode" en vervolgens op "Check for updates". Als er updates zijn, klik dan in het menu links op Updates en installeer deze.
