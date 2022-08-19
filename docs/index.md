---
layout: default
---

**FAQ:** [KHfunctions](./faq-khfunctions.html) - [orgdata](./faq-orgdata.html) | [Rediger](https://github.com/helseprofil/helseprofil.github.io/edit/main/docs/index.md)

Her finner du veiledning om hvordan du kan installere pakker eller bruke funkjonene for KHelse arbeid. For å oppdatere
håndboken kan gjøres direkte i [editor på 
GitHub](https://github.com/helseprofil/helseprofil.github.io/edit/main/docs/index.md)

# Hvordan installerer ...

Installasjon brukes for å sette opp ny maskin eller kjører fersk installasjon.
Det er viktig at du må først installere **Git** fra SoftwareCenter.

### KHfunctions
- Kjør:

```R
source("https://raw.githubusercontent.com/helseprofil/misc/main/utils.R")
kh_restore(khfunctions)
```
- RStudio skal restarte når alle pakkene som brukes i *KHfunctions* har blitt installert og så re-åpne innen *khfunctions* prosjekt.

- I tillegg til ny maskin så trenger du å kjøre komandoen:
  1. Hvis nye pakker eller pakker versjoner har blitt brukt i `KHfunctions.R`. Du bør få beskjed om dette.
  2. Du har oppgradert R versjon

- Du behøver *IKKE* å kjøre komandoen på nytt hvis det bare er endring i kodene. 

- For mer detaljert veileding kan leses [her](https://github.com/helseprofil/khfunctions#khfunctions "khfunctions")

### orgdata
- Kjør:

```R
source("https://raw.githubusercontent.com/helseprofil/misc/main/utils.R")
kh_install(orgdata)
```
- Du får automatisk beskjed i consolen ved pakke *loading* når det kommer ny
  release versjon. For å oppdatere til ny versjon manuelt, kjør:

```R
orgdata::update_orgdata()
```
- For mer detaljert veiledning kan leses [her](https://helseprofil.github.io/orgdata "orgdata")

# Hvordan bruker ...

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
- Eksampler til bruk av de funksjonene for orgdata finnes i [SePaaFil.R](https://helseprofil.github.io/orgdata/articles/sepaafil.html "sepaafil")

# Hvordan vedlikeholder ...

Dette er relevant hvis du skal oppdatere og vedlikeholde funksjonene i *orgdata* eller *khfunctions*.

```R
source("https://raw.githubusercontent.com/helseprofil/misc/main/utils.R")
kh_restore(orgdata)
```

# Load og installerer flere pakker samtidig ... 

Noen ganger trenger man å ha tilgang til flere pakker dvs. både pakker for
KHelse og andre fra CRAN samtidig. Bruk `kh_load()` til det for å *load* pakker.
Hvis pakker ikke finnes lokalt allerede så skal de installeres automatisk før
*loading*. Denne funksjonen gjelder både for pakker tilgjengelig på CRAN og
KHelse relaterte pakker dvs. `orgdata`, `khompare` etc.

```R
source("https://raw.githubusercontent.com/helseprofil/misc/main/utils.R")
kh_load(orgdata, dplyr, ggplot2, norgeo)
```

Den nesten samme funksjonen kan også oppnås ved å bruke `p_load()` fra
[pacman](https://cran.r-project.org/web/packages/pacman/index.html "pacman")
package, men det funker bare for pakker fra CRAN og ikke for de KHelse pakkene. I tillegg må man først
installere `pacman` pakke.


**FAQ:** [KHfunctions](./faq-khfunctions.html) - [orgdata](./faq-orgdata.html)
