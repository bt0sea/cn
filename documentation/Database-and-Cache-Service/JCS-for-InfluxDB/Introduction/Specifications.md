

# 产品规格

云数据库 InfluxDB 目前支持以下规格。

## 实例规格

| 规格代码        | vCPU（核） | 内存（GB） | 每秒写入点数（参考值） | 存储空间（GB） |
| --------------- | ---------- | ---------- | ---------------------- | -------------- |
| tsds.s1.large   | 1          | 4          | 10000                  | 10-1000        |
| tsds.s1.xlarge  | 2          | 8          | 20000                  | 10-1000        |
| tsds.s1.2xlarge | 4          | 16         | 40000                  | 10-1000        |
| tsds.s1.4xlarge | 8          | 32         | 120000                 | 10-1000        |
| tsds.s1.8xlarge | 16         | 64         | 260000                 | 10-1000        |

**说明：**

每秒写入点数与每个数据点包含的字段数量相关，字段越多，每秒写入点数越低。

以上每秒写入点数为每个数据点包含10个字段时的写入速度。

