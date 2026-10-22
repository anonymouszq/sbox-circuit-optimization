# S-box Circuit Results

Circuit files, logic metrics, mapped areas, and timing results for S-box circuit optimization.

## Contents

| File or directory | Description |
| --- | --- |
| `results/logic_results.csv` | 36 logic results: gate counts, circuit depth, nonlinear depth, and mapped area |
| `results/timing_results.csv` | Area, delay, and ADP for 12 circuit pairs at 5 fF and 10 fF; published values, remeasured baselines, and our results are listed separately |
| `circuits/logic/` | 36 logic circuits, identified by L01–L36 |
| `circuits/mapped/` | The corresponding 36 mapped netlists for area evaluation |
| `circuits/timing/` | 48 timing netlists for T01–T12, including baselines and our circuits at both loads |
| `timing_reports/` | The corresponding 48 OpenSTA timing reports |

## Metrics and measurement settings

- **G**: total gate count; **L**: linear gate count; **N**: nonlinear gate count.
- **D**: circuit depth; **DN**: nonlinear depth.
- Area is reported in gate equivalents (GE), delay in ns, and ADP is the area–delay product.

Measurements use the Nangate45 typical cell library at **1.1 V and 25°C**.
OpenSTA 3.1.0 uses a 0.02 ns input transition, output loads of 5 fF or 10 fF,
and zero wire parasitics. These are cell-level static timing results.

The logic and timing tables refer to their respective netlists; metrics from different netlists should not be combined.
All included circuits were verified over their complete input domains.
All 36 mapped areas and 48 timing measurements were rerun and checked against the recorded results.
`CHECKSUMS.sha256` provides file-integrity hashes.
