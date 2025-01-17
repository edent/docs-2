---
title: Basemaps for MapLibre
outline: deep
---

# Basemaps for MapLibre


The `protomaps-themes-base` NPM module contains basemap layer definitions compatible with OpenStreetMap downloads from Protomaps.

```bash
npm install protomaps-themes-base
```
```js
import layers from 'protomaps-themes-base';
```

```js
style: {
    version:8,
    glyphs:'https://cdn.protomaps.com/fonts/pbf/{fontstack}/{range}.pbf',
    sources: {
        "protomaps": {
            type: "vector",
            url: "pmtiles://https://example.com/example.pmtiles",
            //       ^-- Remember to prefix the URL with pmtiles://
            attribution: '<a href="https://protomaps.com">Protomaps</a> © <a href="https://openstreetmap.org">OpenStreetMap</a>'
        }
    },
    layers: layers("protomaps","light")
}
```

the default export from `protomaps-themes-base` is a function that takes 2 arguments:

* the source name of the basemap.

* the theme, one of `light`, `dark`, `white`, `black`, `grayscale` or `debug`.

