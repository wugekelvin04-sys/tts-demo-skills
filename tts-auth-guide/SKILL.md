---
name: tts-auth-guide
description: 详细说明 tts-demo auth login 的完整步骤和注意事项。当用户询问如何登录、授权流程，或遇到登录问题时调用。
---

# TTS Demo CLI — 授权指南

## 运行登录命令

```bash
tts-demo auth login
```

## 流程说明

1. **CLI 启动** → 自动打开浏览器到创建 App 页面
2. **创建 App** → 填写 App 名称，点「创建 App」
3. **自动跳转** → 浏览器自动进入授权页（无需手动操作）
4. **授权** → 确认权限范围，点「授权」
5. **完成** → CLI 终端显示登录成功，凭证自动保存

## 凭证存储

登录完成后，以下凭证存入系统 Keychain（或 `~/.tts-demo/credentials.json`）：
- `app_key` — App 标识
- `app_secret` — App 密钥（本地签名用，不上网）
- `access_token` — 业务调用凭证
- `shop_id` — 店铺 ID

## 重新登录

直接再次运行 `tts-demo auth login` 即可，新凭证会覆盖旧的。

## 排查

- 浏览器未自动打开：手动访问终端显示的 URL
- 服务器连接失败：确认 https://cli.wug.win 可访问
