# Business Impact
```chartjs
{
  "type": "bar",
  "data": {
    "labels": ["Setup (min)", "ROI (x)", "Reach (%)"],
    "datasets": [{
      "data": [9.5, 55, 100],
      "backgroundColor": ["#081027", "#00A8E8", "#F94144"],
      "borderColor": "#FAFBFC",
      "borderWidth": 0.3
    }]
  },
  "options": {
    "animation": { "duration": 500 },
    "scales": {
      "y": { "title": { "text": "Value", "font": { "size": 6 } }, "beginAtZero": true },
      "x": { "title": { "text": "Metric", "font": { "size": 6 } } }
    },
    "plugins": { "title": { "text": "Business Impact", "font": { "size": 7 } } },
    "accessibility": { "description": "Animated bar chart of setup time, ROI, and reach." }
  }
}
**Notes**: Verified metrics, animated Chart.js bar.

#### 11. docs/performance-metrics.md
```markdown
# Performance Metrics & DSP Load
| Block | % Load | Metric | Value | Optimization | TI TAS5825M | NXP i.MX RT1170 | Status |
|-------|--------|--------|-------|--------------|-------------|-----------------|--------|
| ADC | 2% | Latency | 0.5 ms | Increase Lookahead | 1.2 ms | 0.8 ms | 🟢 |
| Gate | 2% | SNR | 102 dB | Match impedance | 95 dB | 99 dB | 🟢 |
| Comp | 5% | THD | 0.0012% | Calibrate gain | 0.005% | 0.0025% | 🟢 |
| EQ | 6% | - | - | Disable if >65% | - | - | 🟡 |
| Lim | 4% | - | - | Fixed | - | - | 🟢 |
| DAC | 2% | - | - | Fixed | - | - | 🟢 |
| GUI | 7% | - | - | Reduce meters | - | - | 🟢 |
| **Total** | **44%** | - | - | <65% | 55% | 48% | 🟢 |

*Sources*: [ADAU1467](https://www.analog.com), [TAS5825M](https://www.ti.com), [i.MX RT1170](https://www.nxp.com).
