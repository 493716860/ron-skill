---
name: wechat-miniprogram
version: 1.0.0
description: Vue3 uni-app TypeScript 电商微信小程序研发规范。
---
# 微信小程序 Skill V1.1
技术栈：Vue3 + uni-app + Vite + TypeScript + Pinia + uni-mini-router + UnoCSS + ESLint + Prettier。UI：Wot Design Uni/uView 待选；HTTP：Alova/自封装 request 待选。SCSS 按需。
## 强制
页面、API、Store、组件、类型分层；统一 /api/v1/mini 请求与 {code,message,data,request_id} 响应；Token 安全存储，401 受控登录；金额、库存、积分、分销佣金、支付状态均以服务端为准；支付结果必须向后端确认；首页装修仅白名单组件和跳转；关键代码必要中文注释。不得硬编码密钥或擅自添加依赖。
## AI 工作流
先读现有代码与对应规则，最小范围修改，检查异常态与交易安全，说明实际验证结果。详见 rules/。

## 营销活动强制规范
限时秒杀、拼团、活动价、优惠券、满减满折、新人专享、会员专享和运营专题专区必须遵循 `rules/marketing.md`。活动资格、库存、价格、成团与退款状态由后端最终确认；小程序只负责交互展示。
