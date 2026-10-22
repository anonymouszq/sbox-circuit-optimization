# S-box Circuit Results

S 盒电路优化的结果与线路文件。

| 文件或目录 | 内容 |
| --- | --- |
| `results/logic_results.csv` | 36 条逻辑结果：门数、深度、非线性门数、非线性深度及映射面积 |
| `results/timing_results.csv` | 12 对线路在 5 fF、10 fF 下的面积、时延和 ADP；分别列出原文公布值、原线路重测值和本文结果 |
| `circuits/logic/` | 36 条逻辑线路，编号 L01–L36 |
| `circuits/mapped/` | 对应的 36 份面积映射网表 |
| `circuits/timing/` | 48 份时序网表，编号 T01–T12，包含原线路与本文线路 |
| `timing_reports/` | 对应的 48 份 OpenSTA 时序报告 |

## 指标与测试条件

G：总门数；L：线性门数；N：非线性门数；D：电路深度；DN：非线性深度。
面积单位为 GE，时延单位为 ns，ADP 为面积与时延的乘积。

使用 Nangate45 typical 单元库（1.1 V、25°C）和 OpenSTA 3.1.0，
输入转换时间为 0.02 ns，输出负载为 5 fF 或 10 fF，不计布线寄生。
这些数据是单元级静态时序结果。

逻辑结果表与时序结果表使用各自对应的网表，不能跨表拼接指标。
所有线路均已全输入验证；36 项映射面积和 48 项时延已重新运行核对。
`CHECKSUMS.sha256` 用于检查文件完整性。
