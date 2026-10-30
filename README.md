# QuantumultX

个人维护的 Quantumult X 配置与规则仓库。基于 [@curtinp118/QuantumultX](https://github.com/curtinp118/QuantumultX) 清爽版配置改造。

## 目录结构

```
├── profile/
│   └── QX_Config.conf        # 主配置（证书/订阅已占位符化）
├── rules/
│   └── hongguo-adblock.list  # 红果短剧/番茄小说去广告分流（199 条）
└── scripts/
    └── hongguo-adblock.conf  # 红果去广告重写（16 条 URL reject）
```

## 导入方法

1. **主配置**：QX → 设置 → 配置 → 引用，填入本仓库 `profile/QX_Config.conf` 的 raw 链接。
2. 导入后需要本地补齐三处占位符（编辑配置文件）：
   - `[server_remote]` 中 `YOUR_AIRPORT_SUBSCRIPTION_URL` → 你的机场订阅链接；
   - `[mitm]` 中 `passphrase` / `p12` → 在 QX 内重新生成证书（配置文件里的占位符可直接删掉这两行再生成）。
3. 红果分流与重写为远程订阅，主配置引用后自动拉取，无需手动操作。

## 规则来源与致谢

- 红果分流：原 `chengaiying99-cmd/QuantumultX` 订阅导出（该仓库已 404）。
- 红果重写：原订阅导出（bytegecko 2 条）+ [doovvip/sublink-worker2](https://github.com/doovvip/sublink-worker2) HongGuo-Surge-Native 增强。
- 原始配置：[@curtinp118/QuantumultX](https://github.com/curtinp118/QuantumultX)。
- Turrit 分流：本地规则，指向 Telegram 策略组。

## 更新日志

- 2026-10-30：Turrit 分流修复；失效订阅（AI/AppleIntelligence）换源 curtinp118；红果分流/重写云端化入库。
