# Vue3 + TypeScript 编码规范
采用 Composition API 和 <script setup lang="ts">。组件 Props/Emits/DTO 定义类型，外部未知值优先 unknown 并做校验；避免 any 和无依据的类型断言。组件 PascalCase，组合函数 useXxx，变量 camelCase，文件命名保持项目一致。ESLint + Prettier 统一格式；公共函数、关键逻辑写准确、必要的中文注释，不逐行翻译。避免超长组件、重复逻辑、深层嵌套与过度封装。组件卸载时清理定时器、监听、请求及 ECharts 实例。
