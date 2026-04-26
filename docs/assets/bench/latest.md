# Patternia Benchmark Report

- Source: `bench_results/ptn_bench.json`
- Scenarios: `5`
- Patternia fastest: `1/5`
- Average Patternia gap vs fastest: `+29.39%`
- Largest Patternia gap: `LiteralMatch` `+100.28%` vs `Switch`

## Patternia Focus

| Scenario | Patternia impl | Rank | Patternia mean (ns) | Fastest | Fastest mean (ns) | Gap vs fastest | Patternia CV % | Status |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| LiteralMatch | PatterniaPipe | 3/3 | 1.799 | Switch | 0.898 | +100.28% | 0.10 | slow |
| CommandParser | PatterniaPipe | 2/4 | 1.774 | Switch | 1.356 | +30.86% | 0.43 | slow |
| ProtocolRouter | PatterniaPipe | 2/4 | 1.678 | StdVisit | 1.496 | +12.17% | 0.90 | watch |
| PacketMixed | PatterniaPipe | 2/2 | 1.507 | Switch | 1.454 | +3.63% | 4.98 | close |
| VariantMixed | PatterniaPipe | 1/4 | 1.060 | PatterniaPipe | 1.060 | +0.00% | 1.00 | fastest |

---

## Per-Scenario Details
### LiteralMatch

| Impl | Mean (ns) | vs fastest | vs Patternia | CV % |
|---|---:|---:|---:|---:|
| Switch | 0.898 | fastest | -50.07% | 0.15 |
| IfElse | 0.909 | +1.20% | -49.47% | 0.24 |
| **PatterniaPipe** | 1.799 | +100.28% | - | 0.10 |

### CommandParser

| Impl | Mean (ns) | vs fastest | vs Patternia | CV % |
|---|---:|---:|---:|---:|
| Switch | 1.356 | fastest | -23.58% | 0.91 |
| **PatterniaPipe** | 1.774 | +30.86% | - | 0.43 |
| IfElse | 1.865 | +37.55% | +5.11% | 3.76 |
| StdVisit | 2.016 | +48.66% | +13.60% | 0.17 |

### ProtocolRouter

| Impl | Mean (ns) | vs fastest | vs Patternia | CV % |
|---|---:|---:|---:|---:|
| StdVisit | 1.496 | fastest | -10.85% | 0.32 |
| **PatterniaPipe** | 1.678 | +12.17% | - | 0.90 |
| Switch | 1.721 | +15.06% | +2.58% | 0.20 |
| IfElse | 1.888 | +26.25% | +12.56% | 0.53 |

### PacketMixed

| Impl | Mean (ns) | vs fastest | vs Patternia | CV % |
|---|---:|---:|---:|---:|
| Switch | 1.454 | fastest | -3.50% | 1.18 |
| **PatterniaPipe** | 1.507 | +3.63% | - | 4.98 |

### VariantMixed

| Impl | Mean (ns) | vs fastest | vs Patternia | CV % |
|---|---:|---:|---:|---:|
| **PatterniaPipe** | 1.060 | fastest | - | 1.00 |
| StdVisit | 1.067 | +0.71% | +0.71% | 0.12 |
| SwitchIndex | 1.086 | +2.49% | +2.49% | 1.09 |
| Sequential | 1.231 | +16.18% | +16.18% | 0.16 |

