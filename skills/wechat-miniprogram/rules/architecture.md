# 目录与分层
src/pages 主包、src/pages-sub 分包、src/components 公共组件、src/api API、src/services 业务编排（按需）、src/stores Pinia、src/composables 组合函数、src/types 类型、src/utils 工具、src/constants 常量、src/styles 样式、src/static 资源、src/config 配置。页面负责交互，API 负责请求，Store 仅管理跨页状态。禁止页面直接拼 URL、跨模块修改 Store 和循环依赖。按微信小程序包体限制按需分包。
