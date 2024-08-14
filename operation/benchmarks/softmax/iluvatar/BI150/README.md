# 参评AI芯片信息

* 厂商：ILUVATAR

* 产品名称：BI150
* 产品型号：BI150
* TDP：W

# 所用服务器配置

* 服务器数量：1


* 单服务器内使用卡数：1
* 服务器型号：
* 操作系统版本：Ubuntu 20.04.6 LTS
* 操作系统内核：linux5.4.0-148-generic
* CPU：
* docker版本：20.10.25
* 内存：
* 服务器间AI芯片直连规格及带宽：此评测项不涉及服务期间AI芯片直连

# 算子库版本
FlagGems:>联系邮箱: contact-us@iluvatar.com获取版本(FlagGems-0710_pointwise_use_tid)

# 评测结果

## 核心评测结果

| 评测项  | 平均相对误差(with FP64-CPU) | TFLOPS(cpu wall clock) | TFLOPS(kernel clock) | FU(FLOPS Utilization)-cputime | FU-kerneltime |
| ---- | -------------- | -------------- | ------------ | ------ | ----- |
| flaggems | 1.02E-07    | 0.14TFLOPS       | 0.14TFLOPS        | 0.59% | 0.59% |
| nativetorch | 7.96E-08    | 0.11TFLOPS      | 0.11TFLOPS      | 0.46%      | 0.46%    |

## 其他评测结果

| 评测项  | 相对误差(with FP64-CPU)标准差 | cputime | kerneltime | cputime吞吐 | kerneltime吞吐 | 无预热时延 | 预热后时延 |
| ---- | -------------- | -------------- | ------------ | ------------ | -------------- | -------------- | ------------ |
| flaggems | 1.36E-09    | 11114.98us       | 11120.17us        | 89.97op/s | 89.93op/s | 445973.49us | 12206.26us |
| nativetorch | 1.67E-09    | 14279.23us       | 14298.75us        | 70.03op/s | 69.94op/s | 14581.57us | 14520.96us |

## 能耗监控结果

| 监控项  | 系统平均功耗  | 系统最大功耗  | 系统功耗标准差 | 单机TDP | 单卡平均功耗 | 单卡最大功耗 | 单卡功耗标准差 | 单卡TDP |
| ---- | ------- | ------- | ------- | ----- | ------------ | ------------ | ------------- | ----- |
| nativetorch监控结果 | 2087.29W | 2109.0W | 38.58W   | /     | 183.82W       | 184.0W      | 1.52W        | 350W  |
| flaggems监控结果 | 2071.0W | 2090.0W | 38.0W   | /     | 177.61W       | 178.0W      | 3.89W        | 350W  |

## 其他重要监控结果

| 监控项  | 系统平均CPU占用 | 系统平均内存占用 | 单卡平均温度 | 单卡最大显存占用 |
| ---- | --------- | -------- | ------------ | -------------- |
| nativetorch监控结果 | 44.578%    | 2.583%   | 49.74°C       | 25.739%        |
| flaggems监控结果 | 43.335%    | 2.578%   | 47.83°C       | 19.489%        |