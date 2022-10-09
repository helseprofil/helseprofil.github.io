---
layout: default
title: Startside
nav_order: 1
description: "Startside"
has_children: true
permalink: /
---

Her finner du veiledning om hvordan du kan installere pakker eller bruke
funkjonene for KHelse arbeid. For å oppdatere håndboken kan gjøres direkte i
[editor på
GitHub](https://github.com/helseprofil/helseprofil.github.io/edit/main/docs/index.md)
eller via link *Rediger direkte på GitHub* nederst på hver side

# Hvordan vedlikeholder ...

Dette er relevant hvis du skal oppdatere og vedlikeholde funksjonene i *orgdata* eller *khfunctions*.

```R
source("https://raw.githubusercontent.com/helseprofil/misc/main/utils.R")
kh_restore(orgdata)

# Eller
kh_restore(khfunctions)
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

