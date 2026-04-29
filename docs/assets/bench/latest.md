# Patternia Benchmark Report

- Source: `bench_results/ptn_bench.json`
- Scenarios: `5`
- Patternia fastest: `1/5`
- Average Patternia gap vs fastest: `+29.24%`
- Largest Patternia gap: `LiteralMatch` `+79.98%` vs `IfElse`

## Patternia Focus

| Scenario | Patternia impl | Rank | Patternia mean (ns) | Fastest | Fastest mean (ns) | Gap vs fastest | Patternia CV % | Status |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| LiteralMatch | PatterniaPipe | 3/3 | 1.581 | IfElse | 0.878 | +79.98% | 1.07 | slow |
| PacketMixed | PatterniaPipe | 2/2 | 1.888 | Switch | 1.442 | +30.91% | 0.60 | slow |
| ProtocolRouter | PatterniaPipe | 2/4 | 1.907 | StdVisit | 1.458 | +30.87% | 0.46 | slow |
| CommandParser | PatterniaPipe | 3/4 | 1.971 | Switch | 1.887 | +4.44% | 0.79 | close |
| VariantMixed | PatterniaPipe | 1/4 | 0.941 | PatterniaPipe | 0.941 | +0.00% | 0.28 | fastest |

---

## Per-Scenario Details
### LiteralMatch

| Impl | Mean (ns) | vs fastest | vs Patternia | CV % |
|---|---:|---:|---:|---:|
| IfElse | 0.878 | fastest | -44.44% | 0.04 |
| Switch | 0.883 | +0.52% | -44.15% | 0.06 |
| **PatterniaPipe** | 1.581 | +79.98% | - | 1.07 |

### PacketMixed

| Impl | Mean (ns) | vs fastest | vs Patternia | CV % |
|---|---:|---:|---:|---:|
| Switch | 1.442 | fastest | -23.61% | 0.26 |
| **PatterniaPipe** | 1.888 | +30.91% | - | 0.60 |

### ProtocolRouter

| Impl | Mean (ns) | vs fastest | vs Patternia | CV % |
|---|---:|---:|---:|---:|
| StdVisit | 1.458 | fastest | -23.59% | 0.61 |
| **PatterniaPipe** | 1.907 | +30.87% | - | 0.46 |
| Switch | 2.098 | +43.94% | +9.99% | 0.63 |
| IfElse | 2.127 | +45.96% | +11.53% | 0.97 |

### CommandParser

| Impl | Mean (ns) | vs fastest | vs Patternia | CV % |
|---|---:|---:|---:|---:|
| Switch | 1.887 | fastest | -4.25% | 0.25 |
| StdVisit | 1.933 | +2.41% | -1.95% | 0.36 |
| **PatterniaPipe** | 1.971 | +4.44% | - | 0.79 |
| IfElse | 2.178 | +15.43% | +10.52% | 0.22 |

### VariantMixed

| Impl | Mean (ns) | vs fastest | vs Patternia | CV % |
|---|---:|---:|---:|---:|
| **PatterniaPipe** | 0.941 | fastest | - | 0.28 |
| StdVisit | 0.953 | +1.23% | +1.23% | 0.07 |
| Sequential | 1.144 | +21.47% | +21.47% | 0.59 |
| SwitchIndex | 1.173 | +24.57% | +24.57% | 0.03 |

