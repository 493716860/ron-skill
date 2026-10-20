# 前端目录与分层
推荐 src/api、assets、components、composables、config、constants、layouts、router、stores、styles、types、utils、views、App.vue、main.ts。页面负责展示交互；api 只定义请求；composables 封装可复用组合逻辑；stores 维护共享状态；通用组件通过 Props/Emits 通信。禁止组件直接拼接 API URL、公共组件反向依赖业务页面、循环依赖和跨模块随意修改 Store。不强制每个页面增加 service，已有项目不同目录先评估而非大规模搬迁。
