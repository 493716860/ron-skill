---
name: api-database-design
version: 1.0.0
description: 将已确认产品需求转换为 OpenAPI 3.1、MySQL 8.4 SQL Migration、数据字典和交易安全详细设计
---
# API 与数据库详细设计 Skill V1.0
## 职责
输入：已确认的产品需求（REQ/BR/PAGE/AC）、HTML 原型、权限矩阵、状态机和现有系统契约。输出：经过审查的技术设计包；不替代产品需求决策，不直接实现业务代码。
## 技术基线
Go 1.25 + Gin + GORM + MySQL 8.4 LTS；JWT（golang-jwt）、Redis 按需、Swagger（swag）。经典分层。生产结构变更只用版本化 SQL Migration，不允许 GORM AutoMigrate。
## P0 强制
1. 先核对输入的需求版本、业务决策与已有 API/表结构；高风险 TBD 不得猜测，阻断研发就绪。
2. 每个 API 具备 API-ID、REQ/BR 来源、Method/Path、鉴权、参数、字段约束、成功/失败响应、状态码、幂等/分页/并发说明。
3. OpenAPI 3.1 YAML 为接口契约唯一权威来源；JSON 响应使用 code/message/data/request_id，分页 list/total/page/page_size；平台回调按其协议例外。
4. 每张表及每个字段必须有准确中文 COMMENT；金额整数分，索引/唯一键/NULL/默认值/时间语义明确；DDL 使用 MySQL 8.4 LTS 版本化 SQL Migration。
5. 涉及资金、库存、支付、退款、积分、佣金的操作必须描述状态机、事务边界、幂等键、并发冲突与补偿/对账策略。
6. API DTO 与数据库持久化模型分离；页面字段→API 字段→表字段的映射须可追溯，不要求每个页面字段都直接入库。
7. API/DDL/数据字典/状态与权限设计不得冲突；既有接口兼容性和迁移风险必须说明。
8. 不臆造有赞开放平台接口或权限；外部系统能力必须先核实。
## 流程
读取需求与现状→识别待决策项→设计 API/表/状态/事务→编写 OpenAPI 与 SQL→一致性审查→交付设计包供人工确认。
## 规则索引
rules/intake.md、api-contract.md、database.md、transaction-consistency.md、security.md、traceability.md、review.md、change-control.md、handoff.md。
## 交付
按 templates/delivery-layout.md。人工确认后才标记 design_status=approved。此 Skill 不要求 CI/CD、性能压测或自动化测试覆盖率门禁。
