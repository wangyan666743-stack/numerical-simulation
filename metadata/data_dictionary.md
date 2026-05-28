# 数据字典

本文件用于记录数据字段名称、单位、坐标系统、计算方法和数据来源。后续新增结果表或分析表时，应同步补充字段说明，避免论文写作和复核时无法追溯。

## 通用字段

| 字段名 | 单位 | 含义 | 来源 |
| --- | --- | --- | --- |
| `run_id` | - | 单次模拟运行编号 | `metadata/run_log.csv` |
| `date` | YYYY-MM-DD | 模拟完成或归档日期 | 人工记录 |
| `case_name` | - | 工况简称 | 人工记录 |
| `software` | - | 使用的软件名称，如 FLAC3D | `manifest.yml` |
| `software_version` | - | 软件版本 | `manifest.yml` |
| `analysis_status` | - | 分析状态：`raw`、`processed`、`analyzed`、`verified` | 人工记录 |

## 建议记录的关键指标

| 字段名 | 建议单位 | 含义 |
| --- | --- | --- |
| `max_subsidence` | mm 或 m | 最大竖向沉降值 |
| `max_horizontal_displacement` | mm 或 m | 最大水平位移值 |
| `influence_range` | m | 采动影响范围 |
| `boundary_deformation` | mm 或 m | 坝体或研究边界处变形值 |
| `advance_distance` | m | 工作面累计推进距离 |
| `mining_height` | m | 采高 |
| `mining_width` | m | 工作面宽度 |

## 坐标和单位约定

- 坐标系统应在每次运行的 `manifest.yml` 中说明。
- 位移、沉降、应力等单位必须在表头或数据说明中写清楚。
- 如果模拟输出单位与论文使用单位不同，应在 `processed/` 数据或分析报告中说明换算关系。

