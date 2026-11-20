# 办理时长与责任交接分析：资料说明

用于分析服务事项在不同承办责任、等待和交接阶段的耗时。记录包含合成事件与不完整时序。

每个 JSON 文件均为 UTF-8 编码。空字符串表示来源没有给出该事实，不等同于零、否或业务终态。标识仅在本项目资料内有意义。

## `cases.json`

字段：id, kind, received_at。共 4 条合成记录。

## `events.json`

字段：id, case, kind, actor, occurred_at, received_at, ref。共 8 条合成记录。

## `limits.json`

字段：kind, version, valid_from, valid_to, minutes。共 3 条合成记录。

## 关系与口径提示

events.case 对应 cases.id；resume.ref 对应 pause 事件；transfer_accept.ref 对应 transfer_offer。未确认的转交和未闭合暂停均有意保留。limits 按事项类别和有效日期生效。
