# Patternia Benchmark Report

- Source: `docs/assets/bench/latest.csv`
- Scenarios: `5`
- Patternia fastest: `2/5`
- Average Patternia gap vs fastest: `+28.77%`
- Largest Patternia gap: `LiteralMatch` `+99.74%` vs `Switch`

## Patternia Focus

| Scenario | Patternia impl | Rank | Patternia mean (ns) | Fastest | Fastest mean (ns) | Gap vs fastest | Patternia CV % | Status |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| LiteralMatch | PatterniaPipe | 3/3 | 1.800 | Switch | 0.901 | +99.74% | 0.10 | slow |
| CommandParser | PatterniaPipe | 2/4 | 1.774 | Switch | 1.343 | +32.09% | 0.46 | slow |
| ProtocolRouter | PatterniaPipe | 2/4 | 1.671 | StdVisit | 1.492 | +12.02% | 1.03 | watch |
| PacketMixed | PatterniaPipe | 1/2 | 1.405 | PatterniaPipe | 1.405 | +0.00% | 3.48 | fastest |
| VariantMixed | PatterniaPipe | 1/4 | 1.069 | PatterniaPipe | 1.069 | +0.00% | 0.72 | fastest |

---

## Per-Scenario Details
### LiteralMatch

| Impl | Mean (ns) | vs fastest | vs Patternia | CV % |
|---|---:|---:|---:|---:|
| Switch | 0.901 | fastest | -49.94% | 1.45 |
| IfElse | 0.908 | +0.75% | -49.56% | 0.25 |
| **PatterniaPipe** | 1.800 | +99.74% | - | 0.10 |

### CommandParser

| Impl | Mean (ns) | vs fastest | vs Patternia | CV % |
|---|---:|---:|---:|---:|
| Switch | 1.343 | fastest | -24.29% | 0.69 |
| **PatterniaPipe** | 1.774 | +32.09% | - | 0.46 |
| IfElse | 1.898 | +41.37% | +7.02% | 3.70 |
| StdVisit | 2.015 | +50.08% | +13.62% | 0.51 |

### ProtocolRouter

| Impl | Mean (ns) | vs fastest | vs Patternia | CV % |
|---|---:|---:|---:|---:|
| StdVisit | 1.492 | fastest | -10.73% | 0.28 |
| **PatterniaPipe** | 1.671 | +12.02% | - | 1.03 |
| Switch | 1.723 | +15.49% | +3.10% | 0.22 |
| IfElse | 1.888 | +26.59% | +13.01% | 0.65 |

### PacketMixed

| Impl | Mean (ns) | vs fastest | vs Patternia | CV % |
|---|---:|---:|---:|---:|
| **PatterniaPipe** | 1.405 | fastest | - | 3.48 |
| Switch | 1.436 | +2.25% | +2.25% | 1.47 |

### VariantMixed

| Impl | Mean (ns) | vs fastest | vs Patternia | CV % |
|---|---:|---:|---:|---:|
| **PatterniaPipe** | 1.069 | fastest | - | 0.72 |
| StdVisit | 1.071 | +0.14% | +0.14% | 0.81 |
| SwitchIndex | 1.086 | +1.60% | +1.60% | 0.73 |
| Sequential | 1.233 | +15.31% | +15.31% | 0.26 |

