# 🚀 Alpha Detection Skill

> **Real-time Crypto Alpha Detection: Never Miss a Pump Again**

[![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-blue)](https://clawhub.com)
[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## 🎯 What It Does

A sub-agent that **scans Twitter and on-chain data 24/7**, detecting pump signals **5-10 minutes before the crowd**. Used by degens to catch $GIRAFFES-type pumps (1.1M → 2.8M in hours).

## ✨ Why This Is Different

| Feature | Alpha Detection | Manual Monitoring |
|---------|----------------|------------------|
| Uptime | 24/7 sub-agent | Your browser tab |
| Speed | 5-10 min early | After pump starts |
| Cost | Free (your compute) | Your time (priceless) |
| Reliability | Never sleeps | You need coffee |

## 📦 Installation

```bash
# 1. Install the skill (if not already)
/skills add alpha-detection

# 2. Initialize configuration
/alpha-detect init
```

## ⚡ Quick Start

```bash
# Monitor top crypto influencers
/alpha-detect start --source twitter:user:calicastle --keywords "meme,pump,whale"

# Add on-chain metrics (optional)
/alpha-detect configure --chain-tokens "0x...:token_addr" --metrics volume,price

# You'll get Discord alerts like:
# 🚨 ALPHA: $GIRAFFES detected @ 14:23
#    Volume spike: +300% in 5min
#    Suggested: Check before FOMO
```

## 🔧 Configuration

Edit `~/.openclaw/workspace/alpha-detection.yaml`:

```yaml
sources:
  twitter:
    accounts: ["calicastle", "crypto_kelly", "whale_alert"]
    keywords: ["meme", "pump", "whale", "low mc"]
  chain:
    tokens: ["0x...:USDC", "0x...:WETH"]
    metrics: ["volume_24h", "price_change_5m", "holder_growth"]
threshold: 0.75  # Confidence score (0-1)
cooldown: 5m     # Avoid spam
notifications:
  discord: "https://discord.com/webhooks/..."
  telegram: "bot_token:chat_id"
```

## 📊 Real Results

> "撒幣哥昨晚用 OpenClaw 做了個自動化 Alpha 偵測器，今天中午抓到的第一個熱點 $GIRAFFES（市值 1.1M 偵測到，最高衝到 2.8M）"
> — [@calicastle](https://x.com/calicastle/status/2021229394724102229)

## 🛠️ For Developers

```javascript
// Customize detection logic
module.exports = {
  async analyzeSignal(tweet, onChainData) {
    const score = await calculateAlphaScore(tweet, onChainData);
    if (score > config.threshold) {
      return { alert: true, confidence: score };
    }
  }
};
```

## 📈 SEO Keywords

`openclaw`, `ai-agent`, `crypto alpha`, `meme coin detector`, `twitter scanner`, `on-chain monitoring`, `degen tools`, `pump detection`, `crypto bot`, `automated trading`

## 🤝 Contribute

Found a better signal? PRs welcome: https://github.com/Undermybelt/skill-alpha-detection

## 📄 License

MIT — use it, fork it, make money with it.

---

*Made with ❤️ by the OpenClaw community*
*Inspiration: 撒幣哥's $1.1M → $2.8M real trade*
