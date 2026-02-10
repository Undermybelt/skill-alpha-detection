# Alpha Detection Skill

> 实时监控 + 信号提取 + 自动警报

## 功能
持续监控指定数据源（Twitter、链上数据、新闻），检测异常信号并触发通知。

## 使用场景
- 加密货币 Alpha 检测
- 趋势监控（meme coin 爆发）
- 市场异动警报
- 社交媒体热点捕捉

## 核心模式
Sub-agent 长时间运行 + 实时触发 + 信号提取

## 命令
```
/alpha-detect start --source twitter:user:calicastle --keywords "meme,alpha,pump"
/alpha-detect stop
/alpha-detect status
```

## 输出
- 检测到信号 → 发送 Discord/Telegram 通知
- 记录到 `memory/alerts/YYYY-MM-DD-HH-MM.md`
- 包含：信号源、时间、置信度、建议行动

## 配置
```yaml
sources:
  - twitter:
      accounts: ["calicastle", "other"]
      keywords: ["meme", "pump", "whale"]
  - chain:
      tokens: ["0x..."]
      metrics: ["volume", "price", "holders"]
threshold: 0.8  # 置信度阈值
cooldown: 5m   # 相同信号冷却时间
```

---
*Skill: alpha-detection*
*Created: 2026-02-11 00:21*
*Inspired by 撒幣哥实战案例*
