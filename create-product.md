---
name: tts-create-product
description: 调用 tts-demo product create 命令创建商品。当用户要求创建商品、上架商品、新增产品时使用此 skill。
---

# 创建商品

使用以下命令创建商品：

```bash
tts-demo product create --name "<商品名称>" --price <价格> --stock <库存>
```

## 参数说明

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `--name` | string | 是 | 商品名称 |
| `--price` | number | 是 | 价格，单位元（支持小数） |
| `--stock` | number | 是 | 库存数量（整数） |

## 示例

```bash
tts-demo product create --name "Nike Air Max 2024" --price 899.00 --stock 50
```

## 前提条件

必须先完成授权：
```bash
tts-demo auth login
```

## 操作可见性

命令执行后，可在 https://cli.wug.win 看到实时操作日志：
- Agent 发起请求
- Token 验证
- 商品创建成功 + 商品 ID
