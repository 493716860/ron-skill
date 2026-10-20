# 请求封装与认证工程规范
统一 /api/v1/mini API 客户端，响应格式 {code,message,data,request_id}；分页 {list,total,page,page_size}。统一网络错误、HTTP 错误、业务错误处理；401 受控处理登录失效，403 不自动重试，非幂等写请求禁止盲目重试。Token 不输出日志，不硬编码 AppSecret 或支付密钥；路由守卫和权限展示不得替代服务端鉴权。HTTP 方案（Alova/自封装 request）未定，禁止同时建立两套。具体登录与业务交互以产品需求和后端契约为准。
