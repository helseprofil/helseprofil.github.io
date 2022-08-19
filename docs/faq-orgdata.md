---
layout: default
---

[Tilbake](./index.html) | [Rediger](https://github.com/helseprofil/helseprofil.github.io/edit/main/docs/faq-orgdata.md)

# orgdata

Noen spørsmål om bruk av orgdata og Access database til orgdata.

### Adversel "Kan ikke legge til post(er) ..." i Access

Du får adverselen når du skal legge `LESID` og `FILGRUPPE` etter at du har lagt
inn `FILNAVN`. Trykk **OK** og flytt cursor ned eller opp. Deretter bør du kunne
legge `LESID` og `FILGRUPPE`.

### Kan ikke lese filen flere ganger i Access

For å kunne lese en fil flere ganger f.eks annen fane i en Excel fil, kan gjøres
ved å velge `Rediger` knappen. Valg `FILID` av filen og IKKE skrive filstien på
nytt siden det allerede finnes i databasen.

### Kan ikke se "" i Access når kodebok for TYPE lik RE defineres

Når en kolonne skal omkodes ved bruk av TYPE lik `RE` til `""` blir symbolen
likevel forsvant eller usynlige når cursor blir flyttet. Løsningen er å skrive
enten `empty` eller `tom` i *TIL* for å gjøre det tydelig. Selvsagt funker det
med `""` også, hvis du vil gjøre det vanskelig for deg selv og andre å se hva
som egentlig definert i kodeboken &#128512;


[Tilbake](./index.html)
