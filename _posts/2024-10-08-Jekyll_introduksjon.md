---
title: Introduksjon til Jekyll
tags: [webutvikling, nybegynner]
date: 2024-10-04 13:50:00 +0200
categories: [webutvikling]
description: Rask oppsumering av min første erfaring med Jekyll
---

# Introduksjon til Jekyll
- Jekyll er et frammeverk for web utvikling som lar deg generere nettsider fra innhold funnet i Markdown filer. Markdown er stort sett plain text, med noen få unntak for symboler som blir brukt til å signalisere for eksempel overskrifter, liste elementer, linker, bilder, osv.
- Alternativ til Jekyll er Hugo.
- Temaer som Chirpy kan installeres sammen med Jekyll, for å håndtere css og generell design av nettsiden.
- I Chirpy må innlegg lagres med filnavn "YYYY-MM-DD-filnavn.md" i mappen "_posts" for at innleggene skal dukke opp.
- alt under _site mappen forsvinner når du starter opp serveren.

```markdown

# overskrift
paragraph a

## mindre overskrift
paragraf b

- liste element a
- liste element b

[ekstern link](https://www.example.com)

![bilde](image.jpg)

```

## Endring av stylesheet
For å redigere innebygd stylesheet må de følgene filer kopieres fra kildekoden recursively til prosjekt mappe. Kildekoden til Chirpy er funnet i /usr/local/rvm/gems/default/gems/jekyll-theme-chirpy-7.1.1/ 

- fra: /kildekode/_sass til: prosjektmappe/_sass. _sass/colors/typography-light.scss inneholder variabler som foreksempler kontrollerer farge til sidebaren.

Kan bruke "inspect element" i nettleser for å undersøke hva forskjellige variabler heter.
Kan bruke følgende kommand til å søke etter variabel navn i filer

```bash
grep -Rnw . -e "variabel-navn"
```

### ulike notater
- du kan lage en ny side ved å opprette en ny fil i mappen _tabs. Spesifiser en layout i front matter greien. f113

### Endring av språk
- språk kan endres i _config.yml konfigurasjons fil, i variabel "lang". språk koden må matche en av filene funnet i /usr/local/rvm/gems/default/gems/jekyll-theme-chirpy-7.1.1/_data/locales
- hvis ønsket språk ikke er tilgjengelig kan du lage din egen fil ved å kopiere en, bytte på navn og oversette innhold. språk filen må også kopieres til ut av kildekoden og til nettside systemet under mappen _data/locales/

---

### endring av farge på sidebar
- bakgrunns farge på sidebar kontroleres av en variabel med navn --sidebar-bg. Den er funnet i /usr/local/rvm/gems/default/gems/jekyll-theme-chirpy-7.1.1/_sass/colors/typography-light.scss
- typography-dark.scss (hvis du vil endre dark mode)
- Bruk "inspect element" i nettleser for å undersøke hva forskjellige variabler heter.

![bilde](/assets/img/skjermbilde.png){: width="500" height="500"}

vennligst gå til følgende filepath `/path/to/a/file.extend`{: .filepath}


---



## legg til statiske bilder
- legg til mappe /assets/img
- markdown syntax for å inkludere bilder:

```markdown
![bilde](/assets/img/skjermbilde.png){: width="400" height="400"}
```

## Problemer med installasjon
- Opplevde problemer når jeg følget en youtube video som gjennomgikk installasjons prosessen av Jekyll. Tilslutt fant jeg i offesiell dokumentasjon av hvis du prøver å installere det på Windows er det anbefalt å bruke en extension i vscode som heter "Dev container". Antar at dette er en slags docker container.

# Ressurser brukt
- https://www.youtube.com/watch?v=F8iOU1ci19Q&pp=ygUGamVreWxs
- https://www.markdownguide.org/cheat-sheet/
- https://chirpy.cotes.page/posts/getting-started/
- https://github.com/cotes2020/jekyll-theme-chirpy
- https://www.youtube.com/playlist?list=PLLAZ4kZ9dFpOPV5C5Ay0pHaa0RJFhcmcB
- https://tranglc.github.io/posts/getting-started/
