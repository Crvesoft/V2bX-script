# V2bX-script (Crvesoft 定制防断流版)

适配 Xboard 面板与 AI 大模型（如 Claude 3.7 Thinking / Gemini Thinking）深度思考长连接场景。

### 特性优化：
1. **默认锁定稳定版本 `v0.0.13`**：完美兼容 Xboard 面板，避免最新版 v0.0.14+ 导致的设备数 API 错误及节点频繁重启问题；
2. **默认内置 600 秒防断流策略**：自动为 Xray 核心注入 `XrayConnectionConfig`（`connIdle: 600`，`uplinkOnly: 300`，`downlinkOnly: 300`），彻底解决大模型长推理中途报 `The stream was interrupted` 的 60 秒断流问题；
3. 开箱即用，安装或生成配置后无需手动修改 JSON。

### 一键安装命令：
```bash
wget -N https://raw.githubusercontent.com/Crvesoft/V2bX-script/master/install.sh && bash install.sh
```

*(备用 main 分支命令)*：
```bash
wget -N https://raw.githubusercontent.com/Crvesoft/V2bX-script/main/install.sh && bash install.sh
```
