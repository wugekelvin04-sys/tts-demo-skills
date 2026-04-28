---
name: tts-getting-started
description: 介绍 TTS Demo CLI 是什么，如何安装，以及有哪些可用命令。当用户询问 TTS Demo CLI 的功能、如何开始使用时调用。
---

# TTS Demo CLI — 快速入门

TTS Demo CLI (`tts-demo`) 是一个 TikTok Shop AgentReady CLI 原型，让 AI Agent 无需处理签名和 token 就能调用 TikTok Shop 开放能力。

## 安装

```bash
npm install -g github:wugekelvin04-sys/tts-demo-cli
```

## 可用命令

| 命令 | 说明 |
|------|------|
| `tts-demo auth login` | 登录并授权（双链路 Device Code 流程） |
| `tts-demo skills install` | 从 GitHub 安装 Skills 到 Claude Code |
| `tts-demo product create` | 创建商品 |

## 首次使用流程

1. 运行 `tts-demo auth login`
2. 浏览器自动打开，填写 App 名称并创建
3. 页面自动跳转授权，点「授权」
4. CLI 完成登录，凭证存入本地 Keychain
5. 使用 `tts-demo product create` 等命令

## 服务端监控

访问 https://cli.wug.win 可实时查看 Agent 的操作日志和商品列表。
