# CHANGELOG ｜ CCB_EX（Hollowbox 个人特化版）内容 Mod 记录

本文件记录 CCB_EX 相对上游（Z-Vanadium/ChineseCiv6BalanceExpanded）的整合与修改内容。
本仓库为 **Hollowbox 个人特化版内容 Mod**，配套平衡 Mod [CCB（ChineseCiv6BalanceHollowboxVersion）](https://github.com/Anglecs/ChineseCiv6BalanceHollowboxVersion) 使用。

> 说明：本仓库仅包含各文明的内容本体（美术 Assets、平台 BLP/XLP、ARTDEF、SQL/Lua 数据等）；数值与机制平衡由 CCB 平衡 Mod 的 `sql/BBG_Expanded/` 层提供。

---

## 2026-08-18｜初始提交：Hollowbox 特化版内容 Mod

### 📦 来源与结构

- 基于 **ChineseCiv6BalanceExpanded** 的内容 Mod；
- 通过 `modinfoCombiner.py` 重新生成 `CCBExpanded.modinfo`（含各文明 `files.xml` 合并）；
- 顶层目录按地理分区组织：`Africa / Asia / Europe / Mediterranean / Meso / NorthAmerica / CIVITASResources / DistrictIcons / Platform`。

### 🆕 本次整合新增（自 BBG_EX 复制，配合 CCB 平衡层使用）

| 文明 | 内容目录 | 备注 |
|---|---|---|
| 奥地利 · 玛丽亚·特蕾西亚 | `Europe/Austria` | 政治联姻 / 特蕾西亚改革 / 边防军 / 咖啡馆 / 大外交官 |
| 泰诺 · 阿娜卡奥娜 | `Meso/Taino` + `Meso/TainoAnacaona` | 瓜蒂亚奥 / 金色之花 / 巴泰球场 / 马卡纳武士 / 阿雷托 / 科努科 |

- `modinfoCombiner.py` 的 `get_mod_folders()` 新增 `Europe/Austria`、`Meso/Taino`、`Meso/TainoAnacaona`；
- 对应平衡层 SQL 与中文本地化见 CCB 仓库 `CHANGELOG.md`（commit `d71ab0f`）。

### 📋 当前包含的文明内容

| 区域 | 文明 |
|---|---|
| Africa | 斯瓦希里 · 阿希拉姆·哈桑（SwahiliAlHasanibn） |
| Asia | 伊斯坎达尔（Iskandar）、马来西亚（Malaysia）、西藏 · 赤松德赞（TibetTrisongDetsen） |
| Europe | 阿尔弗雷德·埃舍尔（AlfredEscher）、**奥地利（Austria）**、俾斯麦（Bismark）、芬兰（Finland）、高卢 · 维钦托利（GaulVercingetorix）、瑞士（Switzerland） |
| Mediterranean | 马其顿 · 奥林匹亚斯（MacedonOlympias）、腓尼基 · 阿希拉姆（PhoeniciaAhiram） |
| Meso | 阿根廷（Argentina）、玛雅 · Te K'inich（MayaTeKinichII）、**泰诺（Taino）**、**泰诺 · 阿娜卡奥娜（TainoAnacaona）**、特奥蒂瓦坎（TheoticuanasTeotihuacan） |
| NorthAmerica | 图勒 · 捕鲸者（CCBThuleWhalemaker）、图勒 · 基维乌克（ThuleKiviuq） |

### 🛠️ 配套脚本

- `modinfoCombiner.py` — 合并各文明 `files.xml` 重新生成 `CCBExpanded.modinfo`（含新增文明的注册）。
- `modInfoCheck.py` / `modInfoRenamer.py` — modinfo 校验与改名辅助。
- `requirements.txt` — 脚本依赖。

### 📁 本次变更文件清单

| 文件 | 变更 |
|---|---|
| `Europe/Austria/` | 新增（内容本体） |
| `Meso/Taino/`、`Meso/TainoAnacaona/` | 新增（内容本体） |
| `CCBExpanded.modinfo` | 重新生成（注册新增文明） |
| `modinfoCombiner.py` | 修改：`get_mod_folders()` 加入新增文明目录 |
| `CHANGELOG.md` | 新增（本文件） |

> 备注：`lang/chinese.xml` 等本地化由 CCB 平衡 Mod 提供；`CCBExpanded.modinfo.bak` 为本地备份，不入库。

---

## 2026-08-20｜新增「波兰·斯坦尼斯瓦夫」内容本体

- `Europe/PolandStanislaw/`（自 BBG_EX 复制，含 Core / ArtDefs / Assets / Platforms / Textures / XLPs）
- `modinfoCombiner.py` 的 `get_mod_folders()` 新增 `Europe/PolandStanislaw`
- 重新生成 `CCBExpanded.modinfo`（XML 校验通过）
- 平衡层与中文本地化见 CCB 仓库 CHANGELOG（P2-8）
