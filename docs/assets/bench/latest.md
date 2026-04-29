# Patternia Benchmark Report

- Source: `bench_results/ptn_bench.json`
- Scenarios: `5`
- Patternia fastest: `2/5`
- Average Patternia gap vs fastest: `+28.40%`
- Largest Patternia gap: `LiteralMatch` `+100.33%` vs `Switch`

## Patternia Focus

| Scenario | Patternia impl | Rank | Patternia mean (ns) | Fastest | Fastest mean (ns) | Gap vs fastest | Patternia CV % | Status |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| LiteralMatch | PatterniaPipe | 3/3 | 1.800 | Switch | 0.899 | +100.33% | 0.28 | slow |
| CommandParser | PatterniaPipe | 2/4 | 1.775 | Switch | 1.365 | +30.04% | 0.24 | slow |
| ProtocolRouter | PatterniaPipe | 2/4 | 1.675 | StdVisit | 1.500 | +11.65% | 0.88 | watch |
| PacketMixed | PatterniaPipe | 1/2 | 1.444 | PatterniaPipe | 1.444 | +0.00% | 5.78 | fastest |
| VariantMixed | PatterniaPipe | 1/4 | 1.068 | PatterniaPipe | 1.068 | +0.00% | 0.32 | fastest |

---

## Per-Scenario Details
### LiteralMatch

| Impl | Mean (ns) | vs fastest | vs Patternia | CV % |
|---|---:|---:|---:|---:|
| Switch | 0.899 | fastest | -50.08% | 0.27 |
| IfElse | 0.908 | +1.08% | -49.54% | 0.24 |
| **PatterniaPipe** | 1.800 | +100.33% | - | 0.28 |

### CommandParser

| Impl | Mean (ns) | vs fastest | vs Patternia | CV % |
|---|---:|---:|---:|---:|
| Switch | 1.365 | fastest | -23.10% | 1.39 |
| **PatterniaPipe** | 1.775 | +30.04% | - | 0.24 |
| IfElse | 1.890 | +38.45% | +6.47% | 3.94 |
| StdVisit | 2.019 | +47.91% | +13.75% | 1.16 |

### ProtocolRouter

| Impl | Mean (ns) | vs fastest | vs Patternia | CV % |
|---|---:|---:|---:|---:|
| StdVisit | 1.500 | fastest | -10.43% | 0.50 |
| **PatterniaPipe** | 1.675 | +11.65% | - | 0.88 |
| Switch | 1.727 | +15.09% | +3.08% | 0.82 |
| IfElse | 1.886 | +25.72% | +12.60% | 0.15 |

### PacketMixed

| Impl | Mean (ns) | vs fastest | vs Patternia | CV % |
|---|---:|---:|---:|---:|
| **PatterniaPipe** | 1.444 | fastest | - | 5.78 |
| Switch | 1.477 | +2.24% | +2.24% | 1.50 |

### VariantMixed

| Impl | Mean (ns) | vs fastest | vs Patternia | CV % |
|---|---:|---:|---:|---:|
| **PatterniaPipe** | 1.068 | fastest | - | 0.32 |
| StdVisit | 1.068 | +0.01% | +0.01% | 0.19 |
| SwitchIndex | 1.086 | +1.64% | +1.64% | 0.26 |
| Sequential | 1.231 | +15.24% | +15.24% | 0.20 |

