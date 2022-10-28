---
layout: default
title: "KHfunctions" 
parent: "Tips and Tricks"
nav_order: 1  
---

### Spore opp funksjoner som brukes til debugging

For å se hvilke funksjoner som brukes eller aktiveres når man kjører
`LagFilgruppe` eller `LagKUBE` kan gjøres ved å definere `show_function` objekt
til `TRUE` etter at man har `source` *KHfunctions.R* filen. 

```r
rm(list = ls())
source("https://raw.githubusercontent.com/helseprofil/misc/main/utils.R")
kh_source(repo = "khfunctions", branch = "master", file = "KHfunctions.R", encoding = "latin1")

show_function <- TRUE
```
