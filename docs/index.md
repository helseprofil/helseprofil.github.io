## Håndbok 

Her finner du veiledning om hvordan du kan installere pakker eller bruke funkjonene for KHelse arbeid. For å oppdatere
håndboken kan gjøres direkte i [editor på 
GitHub](https://github.com/helseprofil/helseprofil.github.io/edit/main/docs/index.md)

## Installasjon

Installasjon brukes for å sette opp ny maskin eller kjører fersk installasjon.
Viktig at du må først installere **Git** fra SoftwareCenter.

### KHfunctions
- Kjør:

```R
source("https://raw.githubusercontent.com/helseprofil/misc/main/utils.R")
kh_restore(khfunctions)
```
- RStudio skal restarte når alle pakkene som brukes i *KHfunctions* har blitt installert og så re-åpne innen *khfunctions* prosjekt.
- Du må kjøre `kh_restore(khfunctions)` på nytt bare hvis nye pakker eller versjoner har blitt brukt i `KHfunctions.R`, men ikke hvis det bare er endring i kodene. Du bør få beskjed om dette. 
- For mer detaljert veileding kan leses [her](https://github.com/helseprofil/khfunctions#khfunctions "khfunctions")

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
- For mer detaljert veiledning kan leses [her](https://helseprofil.github.io/orgdata/articles/sepaafil.html "orgdata")

## Bruker

### KHfunctions
- Sjekk at du er i prosjekt for *khfunctions*.
- Bruk filen `SePaaFil.R` som veileding til hvordan man kan få tilgang til alle funksjonene i KHelse ved å source `KHfunctions.R` fra GitHub.
- Hvis du ikke vil bruke `SePaaFil.R` er det viktig at du kjører komandoen nedenfor først for å kunne ha tilgang til alle funksjonene i *KHfunctions*

```R
rm(list = ls())
source("https://raw.githubusercontent.com/helseprofil/misc/main/utils.R")
kh_source(repo = "khfunctions", branch = "master", file = "KHfunctions.R", encoding = "latin1")
```

### orgdata

- Du må gjøre *orgdata* pakke tilgjenglig ved å kjøre `library(orgdata)`
- Eksampler til bruk av de funksjonene for orgdata finnes i [SePaaFil.R](https://helseprofil.github.io/orgdata/articles/sepaafil.html)

## Vedlikeholder

Dette er relevant hvis du skal oppdatere og vedlikeholde funksjonene i *orgdata* eller *khfunctions*.

```R
source("https://raw.githubusercontent.com/helseprofil/misc/main/utils.R")
kh_restore(orgdata)
```

## Bonus 

Noen ganger trenger man å ha tilgang til flere pakker fra CRAN samtidig. Bruk
`pkg_load()` til det for å *load* pakker evt. installere pakker først hvis ikke finnes allerede. Denne funksjonen gjelder bare for pakker som er tilgjenglig på CRAN.

```R
source("https://raw.githubusercontent.com/helseprofil/misc/main/utils.R")
pkg_load(dplyr, ggplot2, norgeo)
```
