# 参评AI芯片信息

* 厂商：Nvidia


* 产品名称：A100
* 产品型号：A100-40GiB-SXM
* TDP：400W

# 所用服务器配置

* 服务器数量：1


* 单服务器内使用卡数：1
* 服务器型号：DGX A100
* 操作系统版本：Ubuntu 20.04.4 LTS
* 操作系统内核：linux5.4.0-113
* CPU：AMD EPYC7742-64core
* docker版本：20.10.16
* 内存：1TiB
* 服务器间AI芯片直连规格及带宽：此评测项不涉及服务期间AI芯片直连

# 算子库版本

https://github.com/FlagOpen/FlagGems. Commit ID:982781081f5d62856064ae986e8927a31e96c235

# 评测结果

## 核心评测结果

| 评测项  | 平均相对误差(with FP64-CPU) | TFLOPS(cpu wall clock) | TFLOPS(kernel clock) | FU(FLOPS Utilization)-cputime | FU-kerneltime |
| ---- | -------------- | -------------- | ------------ | ------ | ----- |
| flaggems | 2.15E-08    | 2.72TFLOPS       | 2.72TFLOPS        | 0.96% | 0.96% |
| nativetorch | 2.15E-08    | 2.72TFLOPS      | 2.72TFLOPS      | 0.96%      | 0.96%    |

## 其他评测结果

| 评测项  | 相对误差(with FP64-CPU)标准差 | cputime | kerneltime | cputime吞吐 | kerneltime吞吐 | 无预热时延 | 预热后时延 |
| ---- | -------------- | -------------- | ------------ | ------------ | -------------- | -------------- | ------------ |
| flaggems | 3.97E-10    | 6159.64us       | 6160.38us        | 162.35op/s | 162.33op/s | 331867.49us | 6223.51us |
| nativetorch | 3.97E-10    | 6196.01us       | 6199.3us        | 161.39op/s | 161.31op/s | 10710.77us | 6228.87us |

## 能耗监控结果

| 监控项  | 系统平均功耗  | 系统最大功耗  | 系统功耗标准差 | 单机TDP | 单卡平均功耗 | 单卡最大功耗 | 单卡功耗标准差 | 单卡TDP |
| ---- | ------- | ------- | ------- | ----- | ------------ | ------------ | ------------- | ----- |
| nativetorch监控结果 | 1638.0W | 1638.0W | 0.0W   | /     | 257.6W       | 262.0W      | 3.23W        | 1638.0  |
| flaggems监控结果 | 1794.0W | 1794.0W | 0.0W   | /     | 348.58W       | 351.0W      | 3.55W        | 1794.0  |

## 其他重要监控结果

| 监控项  | 系统平均CPU占用 | 系统平均内存占用 | 单卡平均温度 | 单卡最大显存占用 |
| ---- | --------- | -------- | ------------ | -------------- |
| nativetorch监控结果 | 0.638%    | 1.297%   | 48.81°C       | 31.535%        |
| flaggems监控结果 | 0.661%    | 1.3%   | 52.93°C       | 31.352%        |