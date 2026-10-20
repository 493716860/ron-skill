---
name: wechat-miniprogram
version: 1.2.0
description: Vue3 uni-app TypeScript 微信小程序前端工程规范
---
# 微信小程序工程 Skill V1.2
本 Skill 只规定架构、目录、编码风格、组件、状态、路由、请求、安全编码与可维护性，不规定商品、营销、会员、分销等具体业务功能或业务流程。业务需求与验收标准由独立 product-prototyping Skill 及经确认的需求文档管理。
## 技术基线
Vue3 + uni-app + Vite + TypeScript + Pinia + uni-mini-router + UnoCSS + ESLint + Prettier。UI 库 Wot Design Uni/uView 待定；HTTP Alova/自封装 request 待定。不得自行选型。
## 强制工程规范
1. 页面、组件、API、Store、Composables、Types 分工清晰，禁止页面直接拼接接口 URL 或跨模块随意操作状态。
2. Composition API 与 script setup lang="ts"，类型清晰，避免 any；公共函数与关键实现有必要中文注释。
3. 统一 HTTP 请求入口，统一处理响应结构、错误、401、超时与请求取消；敏感信息不得写入代码或日志。
4. 使用后端返回的交易、权限和状态结果；前端不能成为资金与权限最终裁决方。具体业务规则遵循已确认需求。
5. 页面具备通用加载、空态、失败、重试与防重复提交处理；统一路由、组件和样式约定。
6. 最小范围修改，保持既有项目风格，不擅自引入框架或新增业务功能。
## 规则
阅读 rules/architecture.md、coding.md、api-auth.md、ui-ux.md、ai-change-control.md；涉及通用服务端交互参照 rules/integration-boundaries.md。
## 不强制
CI/CD、覆盖率门禁、性能压测、复杂监控与额外中间件；由人工把关。不得虚报验证结果。
