# 数据一致性校验说明

## MySQL

支持全量校验，如需校验请在创建或修改任务时选择校验类型为“全量校验”。

全量任务迁移完成后，可在任务列表页或详情页点击**校验**按钮，执行数据一致性校验。

- 迁移类型为结构+全量迁移时，全量迁移完成后，在列表页可执行数据校验。
- 迁移类型为结构+全量+增量迁移时，在数据校验同时将持续同步增量数据变更。MySQL的全量校验为动态全量校验，已校验完成的数据再次更新后，将不再做校验，如期望执行完整的全量校验，建议源端停止写入后再开启数据校验。

## SQL Server

支持全量校验，如需校验请在创建或修改任务时选择校验类型为“全量校验”。

SQL Server结束迁移后，数据校验将自动执行。

## MongoDB

暂不支持数据一致性校验。

