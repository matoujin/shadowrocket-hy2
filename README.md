# shadowrocket-hy2

魔戒 HY2 分流（**不含节点**）。

## Grok Bot：开代理不行、关代理行（当前主问题）

手机实测现象：Google 开代理可用，但 **Grok Bot 只要开代理就不行**。处理：把 Cursor/Grok/x.ai 相关域名 **强制直连**。

### 立刻可用（二选一）

**A. 更新模块（推荐）**  
配置 → 模块 → 用下面 URL 添加/更新 → 开启；当前配置必须是魔戒订阅。

**B. 不改规则、先救命**  
Shadowrocket → 设置 → **代理通过的应用**（或「按 App 分流」）→ 对 **Grok Bot** 选「直连/不走代理」。

### 模块 URL

- https://raw.githubusercontent.com/matoujin/shadowrocket-hy2/main/mojie-hy2-align.module
- https://cdn.jsdelivr.net/gh/matoujin/shadowrocket-hy2@main/mojie-hy2-align.module
- https://ghfast.top/https://raw.githubusercontent.com/matoujin/shadowrocket-hy2/main/mojie-hy2-align.module

直连域名：`cursor.sh` / `cursor.com` / `cursor-cdn.com` / `anysphere.co` / `grok.com` / `x.ai` / `workos.com` / `sentry.io`（及 keyword cursor/grok）。  
其它外网仍走 `hy2自动选择`（HY2 → PROXY → DIRECT 回落）。

## 其它说明

- 勿单独「使用」仓库 `.conf`（无节点会空组）。  
- 很多「xx-优化」节点会超时；需要代理时优先 **香港HK-HY2**。
