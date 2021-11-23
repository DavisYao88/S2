---
title: S2DataConfig
order: 0
redirect_from:
  - /zh/docs/api
---


数据映射，description

| 参数 | 说明 | 类型 | 默认值 | 必选  |
| :------------- | :----------------- | :--------- | :----- | :--- |
| data           | 原始数据        | `Data[]` | `[]`   |   ✓   |
| totalData        | 总计数据       | `Data[]` | `[]`   |      |
| fields         | 维度指标配置项       | `Fields` |    |   ✓     |
| meta    | 全局化配置表数数据元信息，以度量为单位进行配置。在 `meta` 上的配置将同时影响所有组件的文本信息。 | `Meta[]`  |  |   ✓    |
| sortParams    | 全局化配置表数数据元信息，以度量为单位进行配置。在 `meta` 上的配置将同时影响所有组件的文本信息。 | `SortParams`  |  |   ✓    |

### Data

array object **required**, _default：null_

功能描述： 设置表的数据源数据源为对象集合，例如：

```json
const data = [{
    "area": "东北",
    "province": "吉林",
    "city": "白山",
    "type": "办公用品",
    "sub_type": "纸张",
    "cost": "2",
}, {
    "area": "东北",
    "province": "吉林",
    "city": "白山",
    "type": "办公用品",
    "sub_type": "笔",
    "cost": "3",
}]
```

### Fields

object **必选**,_default：null_

功能描述： 配置表格的维度域，即对应行列维度

| 配置项名称 | 说明     | 类型   | 默认值 | 必选 |
| :------------- | :----------------- | :--------- | :----- | :--- |
| rows           | 行维度列表         | `string[]` | `[]`   |      |
| columns        | 列维度列表         | `string[]` | `[]`   |      |
| values         | 指标维度列表       | `string[]` | `[]`   |      |
| valueInCols    | 指标维度是否在列头 | `boolean`  | `true` |      |

### Meta

array object **必选**,_default：null_

功能描述： 全局化配置表数数据元信息，以度量为单位进行配置。在 meta 上的配置将同时影响所有组件的文本信息。

| 参数 | 说明 | 类型 | 默认值 | 必选  |
| :--| :--------| :--- | :----- | :--- |
| field  |  度量 id | `string` | | ✓   |
| name | 度量名称 | `string`|  | ✓  |
| formatter | 格式化 <br/>数值度量：一般用于格式化数字<br/>文本度量：一般用于做字段枚举值的别名 | `(v: any) => string` | | |

`markdown:docs/common/sort-params.zh.md`

`markdown:docs/common/custom/customTreeItem.zh.md`