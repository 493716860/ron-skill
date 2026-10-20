---
name: product-prototyping
version: 1.0.0
description: 企业级产品需求规格、业务规则、HTML 仿真交互原型与验收标准设计
---
# 产品需求与交互原型 Skill V1.0
## 定位
本 Skill 是业务需求权威来源，负责需求分析、角色、流程、规则、页面交互、字段规格、权限、异常和验收标准。工程架构、代码风格和具体技术实现由独立研发 Skill 管理。
## 默认交付
一份可独立打开的 HTML 仿真交互原型（含功能导航、页面、弹窗、业务规则、字段规格、异常场景、验收标准），附 README；需求较复杂或需自动消费时增加 requirements.json。用户明确要求单文件时所有内容必须内嵌到 index.html。
## P0 强制
1. 先确认业务目标、角色、边界、核心流程和待决策项；不得把推测当成已确认需求。
2. 每个功能必须具有唯一需求编号、前置条件、触发动作、正常/异常结果、权限与验收场景。
3. 原型必须覆盖需求范围内所有主要页面及关键交互，禁止只画静态首页或仅实现新增弹窗。
4. 表单字段明确类型、必填、长度、枚举、默认值、校验时机、错误文案及依赖关系。
5. 涉及金额、积分、佣金、库存、优惠叠加、支付/退款等规则，必须形成决策表和状态流转；未经确认标记 TBD，不能自作决定。
6. 交互模拟与真实后端调用明确区分，演示数据不得冒充真实业务数据。
7. 验收标准采用可验证的 Given/When/Then，覆盖成功、失败、边界和权限。
8. 原型交付须能离线打开、导航可用、关键控件有实际反馈；自查范围覆盖率与未完成项。
## 规则索引
rules/discovery.md、rules/specification.md、rules/interaction.md、rules/fields-validation.md、rules/permissions-states.md、rules/acceptance-traceability.md、rules/html-prototype.md、rules/ai-change-control.md、rules/handoff.md。
## 非职责
不规定 Vue/uni-app/Gin 的项目架构、编码风格、数据库物理字段类型或具体 API 路径。可提出接口需求和数据需求，但最终技术契约由研发设计确认。
