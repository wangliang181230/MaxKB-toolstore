# MySQL 带参查询工具

## 简介

一个连接 MySQL 数据库，执行带参SQL查询的工具。

## 带参查询的优点

- 规避SQL注入的风险；
- 避免 MySQL 对相同SQL的重复解析过程，复用解析结果（如：执行计划），提升性能。

## 参数说明：

- `sql_and_params` (Dict): sql和参数列表
  - 示例：
  ```json
  {
    "sql": "SELECT * FROM user WHERE id = %s",
    "params": []
  }
  ```

- `to_json_str` (Boolean): 结果是否转换为JSON字符串
  - `true`: 输出 JSON字符串
  - `false`: 输出 List
