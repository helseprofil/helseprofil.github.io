---
layout: default
title: "Installasjon"
parent: "Startside"
nav_order: 1  
---

# Hvordan installerer ...

Installasjon brukes for å sette opp ny maskin eller kjører fersk installasjon.
Det er viktig at du må først installere **Git** fra SoftwareCenter.

### KHfunctions
- Sjekk at du ikke er i et prosjekt.
- Kjør:

```R
source("https://raw.githubusercontent.com/helseprofil/misc/main/utils.R")
kh_install(khfunctions)

# Eller
kh_install(khfunctions, path = "C:/Min/Favoritt/Path")
```
- Standard path blir `C:/Users/DittBrukernavn/helseprofil` hvis argument `path` ikke er spesifisert.
- RStudio skal restarte når alle tillegg pakkene har blitt installert og så re-åpne innen *khfunctions* prosjekt.
For å synkronisere alle pakkeversjoner som brukes i *KHfunctions*, kjør:

```R
renv::restore()
```

- I tillegg til ny maskin så trenger du å kjøre komandoen på nytt hvis:
  1. Nye pakker eller oppdatert pakker versjoner har blitt brukt i `KHfunctions.R`. Du bør få beskjed om dette.
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
