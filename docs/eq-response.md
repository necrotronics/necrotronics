# EQ Frequency Response
```chartjs
{
  "type": "line",
  "data": {
    "labels": [20, 80, 200, 1000, 3000, 8000, 20000],
    "datasets": [
      {
        "label": "EQ",
        "data": [-10, -10, 0, 0, 2, 2, 0],
        "borderColor": "#081027",
        "backgroundColor": "#F94144",
        "fill": false,
        "tension": 0.1
      },
      {
        "label": "Reference",
        "data": [0, 0, 0, 0, 0, 0, 0],
        "borderColor": "#00A8E8",
        "borderDash": [3, 3],
        "fill": false
      }
    ]
  },
  "options": {
    "scales": {
      "x": { "title": { "text": "Hz", "font": { "size": 6 } }, "grid": { "lineWidth": 0.2 } },
      "y": { "title": { "text": "dB", "font": { "size": 6 } }, "min": -12, "max": 4, "grid": { "lineWidth": 0.2 } }
    },
    "plugins": {
      "title": { "text": "EQ Response", "font": { "size": 7 } },
      "tooltip": { "enabled": true, "mode": "point" }
    },
    "accessibility": { "description": "Interactive EQ frequency response with hover tooltips." }
  }
}
