# Axios 请求、响应与认证
仅维护一个业务 Axios 实例，统一 Base URL、超时、Token 注入、错误转换和请求取消。业务 JSON Envelope 为 {code,message,data,request_id}，分页为 {list,total,page,page_size}，接口路径前缀 /api/v1/admin。请求/响应 DTO 必须有 TypeScript 类型。401 并发时只执行一次受控登录失效处理；Token 刷新仅在后端明确提供接口时实现；403 不自动重试，非幂等写请求禁止盲目重发。日志、错误提示不得泄露 Token、密码和敏感数据；文件上传下载等协议按实际格式处理。前端权限不代替后端鉴权。
