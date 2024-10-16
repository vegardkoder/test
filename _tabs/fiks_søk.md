---
icon: fas fa-stream
order: 7
title: fiks søk
layout: fix_search
---

- søke resultater skal erstatte hoved innhold når søkefunksjon er brukt
- blir ødelagt når du endrer på følgende html struktur

```html
<div class="flex-mainarea" id="main-wrapper">
        <div class="container d-flex flex-column ">
            hvis ikke i søke modus: vis markdown innhold
            ellers: vis innlegg søke resultater
        </div>
</div>
```

- søkemotor brukt: https://github.com/christian-fei/Simple-Jekyll-Search
- finn ut hvorfor det bryter sammen når endringer på html er endret.
- div med klasse "row flex-grow-1" får "d-none", når søkefeltet som gjør innholdet skjult. "d-none" blir fjernet fra "search-result-wrapper"
