---
icon: fas fa-stream
order: 6
title: ny layout
layout: new-default
---

# Mål
Lag ny "default layout" for chirpy, som tilslutt skal erstatte den nåværende default layout. format: status, melding.
- (ja) flexbox blir tatt ibruk
- (delvis), reduser CSS og HTML klasser
- (delvis), gjør HTML mer semantisk
- (nei), behold original design(utsende messig sett)

## tanker
- light/dark mode kan kan kontrolleres ved å endre på klassenavn til "root div", og en knapp kan endre på klasse navn.
  
- mange nettsider(twitch, youtube, tiktok) har en header på toppen som er struktert slik: 
  <venstre element || midtstilt søkefelt || høyre element>. Usikker på om dette ville passet mitt tilfelle.
- Er ikke kjempe fornøyd med hvor søkefeltet er plassert, men hvis jeg midstiller kan det fort bli trangt.
- venstre baren og høyere baren burde ha størrelser slik at artikkel innhold blir midtstilt.
- burde topbar alltid være synlig?

## bugs
bugs introdusert med ny layout

- søke funksjon fungerer ikke
- "scroll opp til start" knapp fungerer ikke, og er ikke synlig.
- sidebar bredden stemmer ikke mes css spesifisert. Har noe med flex å gjøre. Fungerer no men liker ikke løsningen.
- text i nylig oppdatert har ikke wrapping
