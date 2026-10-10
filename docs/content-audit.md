# 内容核验与证据边界

核验日期：2026-10-09。读取分支main；取得提交：4c5431a70b9c3049d65f91cb137b3a3727d4bb3c。营销稿按此快照撰写，发布前若仓库变更，应复核。

## 已确认的产物

- 主README、案例README、Discovery、Workflow、Architecture、Risks、Acceptance及现有中文文章均已读取。
- 五阶段framework目录与设计文档存在。它们是交付参考，不是生产系统完成证明。
- 额外检查agent/graph.py、agent/nodes/router.py、agent/tools/refund_status.py、connectors/mock/order_system.py：存在LangGraph图、规则路由和Mock查询代码草案。退款工具调用的是Mock数据。本次未运行代码、未验证完整实现、未审计所有组件。

## 可以与不可以宣称

| 分类 | 证据 | 对外表述 |
|---|---|---|
| 已有文档 | 五个设计文档 | 已公开设计参考 |
| 代码文件 | 图、路由、Mock工具源码 | 存在代码草案；未验证运行 |
| 设计方案 | IM、只读工具、规则、人工队列 | 拟议/设计中 |
| 测试计划 | F1–F10、S1–S5、NF1–NF5及160条数据集规划 | 计划；无执行结果 |
| 业务效果 | Discovery目标与访谈估计 | 待验证；不得写已提效、节省成本或降低客诉 |
| 行业数字 | Discovery引用第三方报告 | 本次未核验原始来源；营销稿不使用 |

## 文档冲突与遗漏

1. 主README声明Demo尚未发布、实现待验证，案例README却含docker启动和预期行为；代码目录已有草案。文章采用更保守表述，未复用启动说明作为交付证明。
2. Discovery为B2B商户；案例README使用消费者/CRM表述。本轮以Discovery、Workflow、Architecture的商户IM场景为准。
3. Workflow的success与Architecture的succeeded不同；余额不足原因也存在不同命名。图采用Architecture与Acceptance命名，并明确需统一字典。
4. 工具输出含canceled，主要设计树未展开。图将其列为未展开/未映射状态，建议保守升级；不是声称已实现该分支。
5. Workflow交接为4字段，Architecture扩展12字段，Acceptance验证6关键字段；实现前需统一schema。
6. Risks标记Mitigated只是文档状态，不能证明控制实现或测试通过。
7. Discovery将账户操作列为人工；Workflow中余额不足等分支可自动解释。图与文章区分解释原因和执行操作。
8. Architecture示例“3–5工作日”和人工SLA占位符不构成实际承诺；稿件不把它们当通用业务事实。
9. 160条是数据集行数合计；功能、安全、性能各有独立采样/测试次数，不能直接视为同一已执行套件。
10. 主README与Acceptance部分阈值不同（例如接管准确性）；文章不宣传数字性能门槛，实施时需统一验收来源。

## 源文件

https://github.com/bob798/enterprise-support-agent/blob/main/README.md
https://github.com/bob798/enterprise-support-agent/blob/main/examples/refund-not-received/README.md
https://github.com/bob798/enterprise-support-agent/blob/main/examples/refund-not-received/discovery.md
https://github.com/bob798/enterprise-support-agent/blob/main/examples/refund-not-received/workflow.md
https://github.com/bob798/enterprise-support-agent/blob/main/examples/refund-not-received/architecture.md
https://github.com/bob798/enterprise-support-agent/blob/main/examples/refund-not-received/risks.md
https://github.com/bob798/enterprise-support-agent/blob/main/examples/refund-not-received/acceptance.md
https://github.com/bob798/enterprise-support-agent/blob/main/content/zh/refund-case-study.md
