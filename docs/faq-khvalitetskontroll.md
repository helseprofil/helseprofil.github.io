---
layout: default
title: "FAQ KHvalitetskontroll"
nav_order: 5
---

# KHvalitetskontroll

Noen spørsmål og løsninger om bruk av *KHvalitetskontroll*.

### Brukerfiler

- Brukerfilene ligger i mappen USER
- Du skal primært bruke 'Kvalitetskontroll_del1.Rmd' og 'Kvalitetskontroll_del2.Rmd'
- Alle funksjonene ligger i mappen som heter R. Disse kopieres fra 

### Feil ved oppstart
- Prosjektet kjører noen script fra GitHub ved oppstart, dette krever internettilgang. 

### Finner ikke fil/Feilmelding ved innlasting av fil
- Sjekk om du har tilgang til F-mappene, prosjektet leser filer direkte herfra

### Feil ved interaktiv bruk
- Får du feilmeldinger av typen "Error in select()", "object not found", eller lignende, kan dette skyldes at du ikke har kjørt koden på toppen for å laste inn datafiler og definere parametrene. Disse skal ligge i *Environment*, og hentes herfra av de ulike funksjonene. 
- Har du definert parametrene, men får feilmeldinger av typen "column doesn't exist", sjekk om du har definert et kolonnenavn som ikke eksisterer i datafilene, eller om et kolonnenavn er feilstavet. R er case-sensitivt, så det er viktig at store og små bokstaver blir riktig. I toppen av kodechunken for å definere parametere ligger det også kode for å liste opp alle variablene som finnes i de to datafilene, for å se hva variablene heter. 

### Feil ved generering av rapport
- For at rapporten skal fungere, må alle kodechunkene kjøre uten feil. Sjekk hver kodechunk manuelt og se om det er en som svikter.




