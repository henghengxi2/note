### 单点登录(SSO Single Sign On)无感刷新 access_token

1. access_token 用户登录凭证
2. refresh_token 在 refresh_token 有效期内每隔两个小时用过期的 access_token 和 refresh_token 去请求更新 access_token 来保持用户登录状态，refresh_token 过期后则需要账号密码登录

实现思路：
方案一： 在请求拦截器里利用本地 expires_in 判断 access_token 是否过期
方案二： 在响应拦截器里判断 access_token 是否过期，过期则
刷新 access_token 再发请求

类似 npm 库： axios-auth-refresh
