---
name: web-admin-frontend
version: 1.0.0
description: Vue3 TypeScript Web 运营后台工程架构与代码规范
---
# Web 运营后台工程 Skill V1.0
本 Skill 仅管理工程架构、代码规范、编码风格、组件复用、路由、状态、API、权限展示、图表和安全编码。具体业务功能、流程、字段和验收标准由独立产品需求设计 Skill 与经确认的需求决定。
## 已锁定技术栈
Vue 3 Composition API + Vite + TypeScript + Element Plus + Pinia + Vue Router 4 + Axios + ECharts + ESLint + Prettier。不得擅自替换技术框架或引入另一套 UI/HTTP/状态库。
## 强制规则
1. 页面、API、组件、composables、stores、router、types 分层；简单页面不强制增加 service。
2. 使用 script setup lang="ts"，明确 Props/Emits、DTO 类型；避免无理由 any；公共函数与关键逻辑有必要中文注释。
3. Axios 统一实例、统一 /api/v1/admin 响应与错误处理，401 受控登出/重新登录，禁止非幂等写请求盲目重试。
4. Vue Router 4 统一动态路由、权限守卫、404/403；按钮权限只控制 UI，服务端必须最终授权。
5. Element Plus 表格/表单/弹窗和 ECharts 复用规范统一；组件生命周期和异步请求正确清理。
6. Pinia 只存需要共享的状态，局部交互状态留在组件；禁止跨模块直接改写 Store。
7. 不擅自增加业务功能、修改公共 API 契约、替换依赖或进行无关重构。
## 规则阅读
通用：rules/architecture.md、rules/coding.md、rules/ui-components.md、rules/ai-change-control.md、rules/integration-boundaries.md。
涉及路由权限：rules/routing-permissions.md；涉及共享状态：rules/state.md；涉及接口：rules/api-auth.md；涉及图表：rules/charts.md。
## 不强制
CI/CD、自动化测试覆盖率门禁、压测、复杂监控或微前端；人工按需验收。不得虚报验证结果。
