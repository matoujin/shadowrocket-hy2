# shadowrocket-hy2

魔戒 HY2 分流规则（**不含节点 / 订阅 token**）。

## 开代理就挂（Google 不通）——立刻恢复

公司机实测（2026-10-28）：**HY2 节点正常**（香港HK-HY2 ~70ms），大量「xx-优化」Vmess **超时**（含德国-优化/德国-优化2、日本-优化3、香港-优化 等）。手机若首页钉在死节点，开代理就全挂——跟是否导入我们 conf 无关。

1. Shadowrocket 顶部先关掉代理，或首页改 **直连**，确认国内网页能开  
2. 配置页：**更新魔戒订阅**；若误用过仓库 conf，切回魔戒订阅并「使用配置」；模块可先关掉  
3. 系统设置 → VPN：**关掉**其它 VPN；设置 → Apple 账号 → iCloud → **关掉「专用代理」**（Private Relay）  
4. 首页手动点能用的节点（优先）：**香港HK-HY2** / 新加坡SG-HY2 / 韩国KR-HY2；备选 **香港HK-A** / 新加坡SG-A  
5. **不要用**：德国-优化、德国-优化2、日本-优化3、香港-优化（当前测速超时）  
6. 配置模式用「规则」；DNS 可用 1.1.1.1 / 8.8.8.8  
7. 若 HY2 在当前 WiFi 也不通：换 **蜂窝** 再试（HY2 走 UDP，部分路由会丢）

## 正确用法（推荐）

1. 当前配置保持**魔戒订阅**（首页能看到节点）  
2. 配置 → 模块 → 添加 `.module` URL → 开启  
3. 代理分组 / 首页锁定 **香港HK-HY2**

## 固定更新 URL

### 模块（推荐）

- https://raw.githubusercontent.com/matoujin/shadowrocket-hy2/main/mojie-hy2-align.module
- https://cdn.jsdelivr.net/gh/matoujin/shadowrocket-hy2@main/mojie-hy2-align.module
- https://ghfast.top/https://raw.githubusercontent.com/matoujin/shadowrocket-hy2/main/mojie-hy2-align.module

### conf（模板，勿单独「使用配置」）

- https://raw.githubusercontent.com/matoujin/shadowrocket-hy2/main/mojie-hy2-align.conf

分组：`hy2节点`(只测 HY2) → `hy2自动选择` = fallback(HY2 → PROXY → DIRECT)。
