---
title: Introduksjon til Jekyll
tags: [webutvikling, nybegynner]
date: 2024-10-04 13:50:00 +800
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

## Forsøk på endring av css I chirpy tema
- hadde vært fint om det var en css fil i chirpy som lot meg redigere css, men så langt har jeg ikke funnet noe slikt. 
- Kanskje jeg må endre kildekoden til chirpy frammeverket direkte for å kunne endre på css.
- "Customizing the Stylesheet" delen i offesiell dokumentasjon matcher ikke filsystemet jeg har i prosjektet mitt. Med mindre de snakker om kildekoden til frammeverket direkte? 
- kildekoden til jekyll befinner seg i
```bash
/usr/local/rvm/gems/default/gems/jekyll-theme-chirpy-7.1.1/
```

- problemet med å endre kildekoden er at når nettsiden skal deployes på foreksempel Vercel.com, vil ikke den redigerte versjonen av kildekoden bli brukt.
- ide: muligens mulig å lage en "fork" versjon av jekyll-chirpy frammeverket, og spesifisere at den versjonen skal brukes når deployment oppstår?

### endring av farge på sidebar
- bakgrunns farge på sidebar kontroleres av en variabel med navn --sidebar-bg. Den er funnet i /usr/local/rvm/gems/default/gems/jekyll-theme-chirpy-7.1.1/_sass/colors/typography-light.scss
- typography-dark.scss (hvis du vil endre dark mode)
- Bruk "inspect element" i nettleser for å undersøke hva forskjellige variabler heter.

![bilde](/assets/img/skjermbilde.png)


## legg til statiske bilder
- legg til mappe /assets/img
- oppgi følgende i innlegg markdown fil når du vil inkludere et statisk bilde.

```markdown
![bilde](/assets/img/filnavn.png)
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
