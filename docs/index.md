## Håndbok 

Hvordan installerer pakker og bruker funkjonene i KHelse arbeid. For å oppdatere håndboken kan gjøres direkte i [editor on GitHub](https://github.com/helseprofil/helseprofil.github.io/edit/main/docs/index.md) 

## Installasjon

Det brukes for å sette opp ny maskin. Viktig at du må først installere **Git** fra SoftwareCenter.

### KHfunctions
- Kjør:

```R
source("https://raw.githubusercontent.com/helseprofil/misc/main/utils.R")
kh_restore(khfunctions)
```
- RStudio skal restarte når alle pakkene som brukes i *KHfunctions* har blitt installert og reåpne innen *khfunctions* prosjekt.
- Hvis *KHfunctions.R* bruker nye pakker så må du kjøre `kh_restore(khfunctions)` på nytt.

### orgdata
- Kjør:

```R
source("https://raw.githubusercontent.com/helseprofil/misc/main/utils.R")
kh_install(orgdata)
```
- For å oppdatere til ny versjon:

```R
library(orgdata)
update_orgdata()
```

## Bruker

### KHfunctions
- Sjekk at du er i prosjekt for *khfunctions*.
- Bruk filen `SePaaFil.R` som veileding til hvordan man kan få tilgang til alle funksjonene i KHelse ved å source `KHfunctions.R` fra GitHub.
- Hvis du ikke vil bruke `SePaaFil.R` er det viktig at du kjøre følgende først for å kunne ha tilgang til alle funkjonene i *KHfunctions*

```R
rm(list = ls())
source("https://raw.githubusercontent.com/helseprofil/misc/main/utils.R")
kh_source(repo = "khfunctions", branch = "master", file = "KHfunctions.R", encoding = "latin1")
```

### orgdata

- Du må gjøre *orgdata* pakke tilgjenglig ved å kjøre `library(orgdata)`
- Eksampler til bruk av de funksjonene for orgdata finnes i [SePaaFil.R](https://helseprofil.github.io/orgdata/articles/sepaafil.html)

## Vedlikehold

Dette er relevant hvis du skal oppdatere funksjonene i *orgdata* eller *khfunctions*.

```R
source("https://raw.githubusercontent.com/helseprofil/misc/main/utils.R")
kh_restore(orgdata)
```
