<p align="center">
  <img src="docs/banner.png" alt="Hellraiser Revival 的 Ketamine Menu" width="100%">
</p>

<h1 align="center">Hellraiser Revival Ketamine 菜单</h1>

<p align="center"><a href="README.md">English</a> · <a href="README.zh-CN.md">简体中文</a></p>

<p align="center">
  为 PC 版 <b>Clive Barker's Hellraiser: Revival</b> 打造的简洁游戏内修改菜单。<br>
  将一个文件放进游戏目录，按下 <kbd>Insert</kbd> 即可使用。
</p>

<p align="center">
  <a href="https://github.com/literalynn/Hellraiser-Revivals-Ketamine-Menu/releases/latest"><img alt="最新版本" src="https://img.shields.io/github/v/release/literalynn/Hellraiser-Revivals-Ketamine-Menu?color=AC6EE2&label=download"></a>
  <a href="https://www.nexusmods.com/clivebarkershellraiserrevival/mods/27"><img alt="Nexus Mods" src="https://img.shields.io/badge/Nexus%20Mods-Ketamine%20Menu-F89FCD"></a>
  <a href="https://github.com/literalynn/Hellraiser-Revivals-Ketamine-Menu/actions/workflows/build.yml"><img alt="构建状态" src="https://github.com/literalynn/Hellraiser-Revivals-Ketamine-Menu/actions/workflows/build.yml/badge.svg"></a>
  <img alt="游戏版本" src="https://img.shields.io/badge/game-1.1.1.227384-F89FCD">
  <img alt="平台" src="https://img.shields.io/badge/platform-Windows%2010%20%2F%2011%20x64-1B1B23">
  <a href="LICENSE"><img alt="MIT 许可证" src="https://img.shields.io/badge/license-MIT-AC6EE2"></a>
</p>

<p align="center">
  <a href="#安装">安装</a> ·
  <a href="#功能">功能</a> ·
  <a href="#使用菜单">使用方法</a> ·
  <a href="#常见问题与故障排除">常见问题</a> ·
  <a href="#卸载">卸载</a> ·
  <a href="#从源代码构建">构建</a>
</p>

---

> [!TIP]
> 使用前请**备份存档**：`%LOCALAPPDATA%\Hellraiser\Saved\SaveGames`。

## 安装

只需一个文件，无需在电脑上安装其他组件（不需要 Visual C++ 运行库或启动器）。

1. 从 [Releases 页面](https://github.com/literalynn/Hellraiser-Revivals-Ketamine-Menu/releases/latest)下载最新的 `KetamineMenu-vX.Y.Z.zip` 并解压。
2. **打开游戏目录**：在 Steam 中右键点击 *Clive Barker's Hellraiser: Revival* → **管理** → **浏览本地文件**。
   然后依次打开 `Hellraiser` → `Binaries` → `Win64`（其中应有 `Hellraiser-Win64-Shipping.exe`）。
3. **将 `winmm.dll` 复制到 `Win64` 文件夹。** 也可以一并复制 `KetamineMenu.ini`（默认设置）。
4. **启动游戏**，读取存档，然后按 <kbd>Insert</kbd>。

```
Clive Barker's Hellraiser - Revival\
└─ Hellraiser\
   └─ Binaries\
      └─ Win64\
         ├─ Hellraiser-Win64-Shipping.exe
         ├─ winmm.dll            ← Ketamine 菜单
         └─ KetamineMenu.ini     ← 可选；否则会自动创建
```

**Vortex：** 前往 [Nexus Mods 页面](https://www.nexusmods.com/clivebarkershellraiserrevival/mods/27)，使用 *Mod Manager Download* 下载。

**手动“解压到游戏目录”：** 请使用 `KetamineMenu-vX.Y.Z-Nexus.zip`。压缩包已包含 `Hellraiser\Binaries\Win64\` 目录结构，可由 Vortex 安装到正确位置，也可以直接解压到游戏目录。

> [!TIP]
> 如果按 <kbd>Insert</kbd> 没有反应，请查看 DLL 同目录下的 `KetamineMenu.log`；日志会说明检测到了什么以及缺少什么。
> 另请参阅[常见问题](#常见问题与故障排除)。

## 功能

所有选项都会在运行时按名称查找游戏数据。如果游戏更新移除了某项内容，对应选项会变灰并在工具提示中说明原因，而不是导致崩溃。

<table>
<tr>
<td width="50%" valign="top">

**玩家**
- 无敌模式、生命值不减
- 生命值滑块（可设置任意值）
- 移除冲刺冷却（游戏没有耐力值）
- 敌人无法发现你
- 一击必杀、伤害倍率

**战斗**
- 无限弹药
- 近战武器永不损坏
- 创世配置能力不消耗苦痛值
- 移除能力冷却、补满苦痛值

**移动**
- 飞行和穿墙；朝视线方向移动，可使用常规移动按键或手柄
- 自由视角（角色留在原地）
- 速度和跳跃高度倍率
- 3 个可保存位置 + 传送到任意关卡检查点

</td>
<td width="50%" valign="top">

**透视**
- 敌人：方框、生命条、名称、距离、骨骼、头部标记、透视高亮、追踪线、屏幕外箭头
- 世界物件：地面物品、战利品容器、存档点
- 可分别设置敌人和物件的显示距离

**背包**
- 增加或移除金钱
- 给予任意物品：弹药、武器、升级、治疗物品、材料（物品列表直接从游戏读取）
- 解锁武器皮肤和挂饰

**世界**
- 时间倍率（慢动作 / 快进）
- 冻结敌人、击杀附近敌人
- 视野范围调整（50° 至 130°，即时生效）、隐藏游戏界面

**进度**
- 查看进行中和已完成的目标、完成目标、更改商店等级

</td>
</tr>
</table>

### 截图

以下截图可能展示旧版英文界面；当前版本的菜单已提供简体中文。游戏内物品名、敌人名和目标名来自游戏数据，保留游戏原文。

<table>
<tr>
<td><img src="docs/menu-player.png" alt="玩家选项卡"></td>
<td><img src="docs/menu-combat.png" alt="战斗选项卡"></td>
</tr>
<tr>
<td><img src="docs/menu-movement.png" alt="移动选项卡"></td>
<td><img src="docs/menu-esp.png" alt="透视选项卡"></td>
</tr>
<tr>
<td><img src="docs/menu-world.png" alt="世界选项卡"></td>
<td><img src="docs/menu-settings.png" alt="设置选项卡"></td>
</tr>
</table>

## 使用菜单

| | |
|---|---|
| <kbd>Insert</kbd> | 打开 / 关闭菜单（可在**设置**中重新绑定）。菜单打开时，鼠标用于操作菜单，游戏会忽略其他输入。 |
| 快捷键 | 可在**设置 → 快捷键**中为每个开关单独绑定按键。菜单关闭时快捷键仍有效，并会显示简短提示。 |
| 悬停 | 将鼠标悬停在选项上，可查看功能说明或不可用的原因。 |
| 界面缩放 | 默认根据屏幕分辨率自动调整；可在**设置**中使用 − / + 按钮调整。 |
| 页脚 | 菜单底部会显示游戏版本、CPU、GPU、内存、分辨率和 FPS。 |
| 设置文件 | 所有设置保存到 DLL 同目录下的 `KetamineMenu.ini`。**设置 → 重置配置**可恢复默认值。 |

> [!WARNING]
> 给予关键物品或完成目标可能会破坏脚本剧情流程。**请先保存游戏。**

## 兼容性

- **游戏：** 已在版本 `1.1.1.227384`（Steam，2026 年 10 月更新）和 `1.0.1.227219` 上测试。其他版本也可能兼容；无法识别的项目会显示为灰色。
- **渲染器：** DirectX 12（默认）和 DirectX 11。
- **其他模组：** 菜单使用 `winmm.dll`，不会与 ReShade（`dxgi.dll`）或 UE4SS（`dwmapi.dll`）冲突。
- **帧生成**（DLSS-G、FSR、XeSS FG）：支持；如果菜单闪烁，请关闭帧生成。
- **中文字体：** 菜单会尝试使用 Windows 中的微软雅黑、黑体、宋体或等线字体。若系统未安装这些字体，菜单会回退到内置字体，中文可能无法正常显示。

## 常见问题与故障排除

<details>
<summary><b>按 Insert 没有反应</b></summary>

- 确认 `winmm.dll` 位于 `Hellraiser\Binaries\Win64`（与 `Hellraiser-Win64-Shipping.exe` 同目录），而不是游戏根目录。
- 打开同目录下的 `KetamineMenu.log`。如果日志不存在，说明 DLL 没有加载；请再次检查文件位置和杀毒软件设置。
- 如果重新绑定了菜单键，菜单页脚和 `KetamineMenu.ini` 的 `[Menu] Key=` 中会显示当前按键。
</details>

<details>
<summary><b>所有选项都显示为灰色</b></summary>

请先读取存档：大多数选项需要玩家角色存在。如果标题区域显示“引擎未连接”，说明游戏版本发生了菜单暂不支持的变化。请提交 Issue 并附上 `KetamineMenu.log`。
</details>

<details>
<summary><b>杀毒软件提示 DLL 有风险</b></summary>

修改器需要接入游戏渲染和内存，因此容易触发杀毒软件的启发式检测。这通常是误报：源代码就在此处，每个发行版本都由 [GitHub Actions](https://github.com/literalynn/Hellraiser-Revivals-Ketamine-Menu/actions) 从源代码构建。你也可以[自行构建](#从源代码构建)。
</details>

<details>
<summary><b>游戏更新后有功能失效</b></summary>

无法找到的选项会变灰并显示原因。请提交 Issue，并附上 `KetamineMenu.log` 和游戏版本（游戏目录中的 `Version.txt`）。
</details>

<details>
<summary><b>如何报告错误？</b></summary>

请[提交 Issue](https://github.com/literalynn/Hellraiser-Revivals-Ketamine-Menu/issues)，说明操作步骤、实际结果，并附上最近一次游戏会话生成的 `KetamineMenu.log`（每次启动游戏都会覆盖该日志）。
</details>

## 卸载

从 `Hellraiser\Binaries\Win64` 删除 `winmm.dll`、`KetamineMenu.ini`、`KetamineMenu.log`（如果使用 Nexus 压缩包安装，还要删除 `KetamineMenu-LICENSE.txt`）。使用 Vortex 安装时，请先移除模组，再删除其留下的 `.ini` 和 `.log` 文件。此菜单不会修改任何游戏文件。

## 从源代码构建

要求：Windows、Visual Studio 2022 或更高版本（包含 *使用 C++ 的桌面开发* 工作负载）、CMake 3.25 或更高版本。

```bash
cmake -S . -B build -A x64
cmake --build build --config Release
ctest --test-dir build -C Release
```

生成的 DLL 位于 `build\Release\winmm.dll`。CMake 会以固定版本和校验和下载 Dear ImGui 与 MinHook。
推送 `v*` 标签会自动构建发行版压缩包。

<details>
<summary><b>工作原理</b></summary>

- **加载：** 游戏会导入 `winmm.dll`，因此 Windows 会优先从游戏目录加载本项目的 DLL。所有 `winmm` 函数都会转发给系统原版 DLL，随后菜单在独立线程中启动。
- **叠加层：** 使用 [MinHook](https://github.com/TsudaKageyu/minhook) 挂钩 DXGI `Present`（DirectX 11 和 12），并通过 [Dear ImGui](https://github.com/ocornut/imgui) 绘制菜单。菜单关闭时不会绘制内容（已启用的通知和透视功能除外）。
- **访问游戏：** 读取虚幻引擎 5 自带的反射数据。仅通过特征码定位三个引擎结构（对象列表、名称表和 `ProcessEvent`）；之后所有类、属性和函数都按名称查找，因此大多数游戏更新不会使其失效。游戏函数通过 `ProcessEvent` 挂钩在游戏线程中调用。
- **安全性：** 所有功能均由崩溃保护机制执行；缺少必要内容时，对应选项会变灰。
</details>

## 致谢

- [Dear ImGui](https://github.com/ocornut/imgui)（MIT）和 [MinHook](https://github.com/TsudaKageyu/minhook)（BSD-2-Clause）
- [Dumper-7](https://github.com/Encryqed/Dumper-7)，用于研究游戏类结构
- [Inter](https://github.com/rsms/inter) 字体（SIL Open Font License 1.1）

## 免责声明

Ketamine Menu 是粉丝制作的工具，与 Saber Interactive、Boss Team Games 或 Clive Barker 均无关联，也未得到其认可。所有商标归各自所有者所有。使用风险由用户自行承担。

## 许可证

[MIT](LICENSE)
