# shadowrocket-hy2

魔戒 HY2 对齐 Mac Clash 的 Shadowrocket 分流（**只含规则与策略组，不含节点密码 / 订阅 token**）。

## 变慢时先做这三步（Grok Bot 变慢专用）

1. Shadowrocket 首页 → **代理分组** → 点开 `hy2自动选择` → **手动选「香港HK-HY2」**（公司机实测约 55ms，通常最快）。
2. 若分组里是空的 / 没有 HY2 节点：说明你用「完整 conf」把魔戒订阅节点顶掉了。**切回魔戒订阅配置**，再用下面的 **模块 URL** 叠加规则（不要只用无节点的 conf）。
3. 配置页把本仓库配置/模块点一次「更新」，拉到修好 DNS、测速间隔 30 秒的版本。

## 固定更新地址（无 commit hash）

### 模块 `.module`（推荐：叠在魔戒订阅上）

- GitHub raw：https://raw.githubusercontent.com/matoujin/shadowrocket-hy2/main/mojie-hy2-align.module
- jsDelivr：https://cdn.jsdelivr.net/gh/matoujin/shadowrocket-hy2@main/mojie-hy2-align.module
- 加速（ghfast）：https://ghfast.top/https://raw.githubusercontent.com/matoujin/shadowrocket-hy2/main/mojie-hy2-align.module

### 完整配置 `.conf`（仅当你已把节点复制进配置时用）

- GitHub raw：https://raw.githubusercontent.com/matoujin/shadowrocket-hy2/main/mojie-hy2-align.conf
- jsDelivr：https://cdn.jsdelivr.net/gh/matoujin/shadowrocket-hy2@main/mojie-hy2-align.conf
- 加速（ghfast）：https://ghfast.top/https://raw.githubusercontent.com/matoujin/shadowrocket-hy2/main/mojie-hy2-align.conf

用法见 `用法-大白话.md`。
