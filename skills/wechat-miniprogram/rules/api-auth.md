# API 与认证
API 前缀 /api/v1/mini；Envelope {code,message,data,request_id}，分页 {list,total,page,page_size}。请求统一入口；区分网络、超时、HTTP、业务错误。401 受控登录，403 不自动重试，非幂等请求不得盲目自动重发。Token 统一安全存储/退出清理，禁止日志输出 Token、支付参数；微信登录凭证交后端交换，小程序不保存 AppSecret、商户密钥。上传/支付遵循平台协议。Alova/自封装 request 待确认，不得并存两套。
