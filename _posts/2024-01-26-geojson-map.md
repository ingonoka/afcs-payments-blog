---
layout: post
title: a post with geojson
date: 2024-01-26 17:57:00
description: this is what included geojson code could look like
tags: formatting charts maps
categories: sample-posts
map: true
---

This is an example post with some [geojson](https://geojson.org/) code. The support is provided thanks to [Leaflet](https://leafletjs.com/). To create your own visualization, go to [geojson.io](https://geojson.io/).


```geojson
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "properties": {
        "title": "Test",
        "stroke": "#555555",
        "stroke-width": 2,
        "stroke-opacity": 1,
        "fill": "#555555",
        "fill-opacity": 0.5
      },
      "geometry": {
        "coordinates": [
          [
            [
              120.62399171100134,
              15.33606579029761
            ],
            [
              120.62399171100134,
              15.298975738791754
            ],
            [
              120.70092372940161,
              15.298975738791754
            ],
            [
              120.70092372940161,
              15.33606579029761
            ],
            [
              120.62399171100134,
              15.33606579029761
            ]
          ]
        ],
        "type": "Polygon"
      },
      "id": 0
    },
    {
      "type": "Feature",
      "properties": {
        "title": "Test"
      },
      "geometry": {
        "coordinates": [
          120.66489040683956,
          15.340346191372205
        ],
        "type": "Point"
      },
      "id": 1
    }
  ]
}
```
