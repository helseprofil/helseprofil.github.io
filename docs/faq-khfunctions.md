---
layout: default
title: "FAQ KHfunctions"
nav_order: 3
---

# KHfunctions

Her finner man spørsmål og løsninger til ymse problemer for *KHfunctions*.

### Får ikke installere

Hvis du får feilmelding når du kjører `kh_install(khfunctions)` kan du gjøre en av disse:

1. Slett mappen `khfunctions` fra `C:/Users/DinBrukerNavn/helseprofil`.
2. Spesifisere `path` der du vil installere `khfunctions` eg.

```r
kh_install(khfunctions, path = "C:/Users/You/FolderName")
```

### Omkode flere input til samme output

Bruk av *TYPE* `KB` i kodebok for omkoding kan bare håndtere en-til-en omkoding.
Men hvis det er behov å omkode flere verdier til en felles verdi i samme
kolonne, kan man bruke *TYPE* `RE` dvs. regulæruttryk, istedenfor. For eksample
å omkode kolonne *INNVKAT* med verdi 1 til 3, til 8 kan defineres slik:

Med `RE`:

| LESID | KOL     | TYPE | FRA     | TIL |
|-------|---------|------|---------|-----|
| ver1  | INNVKAT | RE   | 1\|2\|3 | 8   |

Med `KB`:

| LESID | KOL     | TYPE | FRA | TIL |
|-------|---------|------|-----|-----|
| ver1  | INNVKAT | KB   | 1   | 8   |
| ver1  | INNVKAT | KB   | 2   | 8   |
| ver1  | INNVKAT | KB   | 3   | 8   |

