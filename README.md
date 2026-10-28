# shadowrocket-hy2

魔戒 HY2 分流规则（**不含节点 / 订阅 token**）。

## 紧急恢复（导入后 Google 打不开）

1. Shadowrocket → 底栏「配置」→ 点原来的**魔戒订阅** →「使用配置」
2. 「模块」里先**关掉**「魔戒 HY2 对齐 Mac」
3. 首页选任意可用节点，确认 Google 能开
4. 再按下面「正确用法」只加**模块**

根因：单独使用仓库 `.conf` 时没有节点，`hy2自动选择` 空组 + FINAL 指向它 = 外网全断。

## 正确用法（推荐）

1. 当前配置保持**魔戒订阅**（首页能看到节点列表）
2. 配置 → 模块 → 用 URL 添加下面的 `.module` → 开启
3. 首页「代理分组」里可手动点「香港HK-HY2」

## 固定更新 URL

### 模块（推荐）

- https://raw.githubusercontent.com/matoujin/shadowrocket-hy2/main/mojie-hy2-align.module
- https://cdn.jsdelivr.net/gh/matoujin/shadowrocket-hy2@main/mojie-hy2-align.module
- https://ghfast.top/https://raw.githubusercontent.com/matoujin/shadowrocket-hy2/main/mojie-hy2-align.module

### conf（模板，勿单独「使用配置」）

- https://raw.githubusercontent.com/matoujin/shadowrocket-hy2/main/mojie-hy2-align.conf

新版分组：`hy2节点`(只测 HY2) → `hy2自动选择` = fallback(`hy2节点`,`PROXY`,`DIRECT`)，避免再空组断网。
