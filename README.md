# HideTray

> 一款常驻 macOS 菜单栏的小工具，一键隐藏 / 展开菜单栏图标。
> A lightweight macOS menu-bar utility that hides and reveals your menu-bar icons with one click.

[![Download](https://img.shields.io/badge/Download-HideTray.dmg-blue)](https://github.com/bennix/macHideTray/releases/latest)

---

## 中文

### 简介
HideTray 常驻在你的 macOS 菜单栏，把不常用的图标“挤”出可见区域，让顶栏保持清爽。点一下展开，再点一下折叠。原理与 Hidden Bar / Dozer / Ice 相同（**分隔符挤压法**）——纯公开 API、零权限、稳定。

### 功能
- **一键折叠 / 展开**：左键点开关图标即可切换。启动后默认折叠。
- **自动收回**：展开后超时（可设 3 / 5 / 10 秒 / 永不）或点击菜单栏外任意处即收回。
- **开机自启**：基于 `SMAppService`，可在右键菜单里开关。
- **多语言**：简体中文 / 繁體中文 / English / 日本語。
- **轻量无权限**：不使用辅助功能或私有 API。

### 安装
1. 到 [Releases](https://github.com/bennix/macHideTray/releases/latest) 下载 `HideTray.dmg`。
2. 打开 DMG，把 **HideTray** 拖到 **Applications** 文件夹。

### ⚠️ 首次打开（重要）
本应用**未经 Apple 公证（notarize）**，从网络下载后 macOS 第一次会拦截，提示“无法打开，因为 Apple 无法检查其是否包含恶意软件”。这是 macOS 对未公证应用的**标准安全提示，并非病毒**。任选一种方法，**只需做一次**：

- **方法 A（推荐）**：在「应用程序」里 **右键（或 Control + 单击）HideTray → 打开 → 再点“打开”**。之后即可正常双击。
- **方法 B**：右键打开 DMG 里的 `允许打开 Allow-Open.command` 助手脚本。
- **方法 C**：终端执行
  ```bash
  xattr -dr com.apple.quarantine /Applications/HideTray.app
  ```

### 使用
- **左键** 开关图标：展开 / 折叠隐藏的图标。
- **右键** 开关图标：菜单（开机自启、自动收回延时、语言、退出）。
- **决定藏谁**：按住 **⌘** 拖动菜单栏图标排序——分隔线**左侧**的图标会被隐藏。

### 已知限制
隐藏粒度是“分隔线左边一整片”，不能逐个精确挑选。通过 ⌘ 拖动排序来决定哪些图标被隐藏。

---

## English

### Overview
HideTray lives in your macOS menu bar and squeezes rarely-used icons out of the visible area to keep the top bar clean. Click to expand, click to collapse. It uses the same **separator-squeeze** technique as Hidden Bar / Dozer / Ice — public APIs only, no permissions, rock-solid.

### Features
- **One-click collapse / expand** — left-click the toggle icon. Starts collapsed.
- **Auto-collapse** — after a timeout (3 / 5 / 10 s / Never) or when you click anywhere outside the menu bar.
- **Launch at login** — via `SMAppService`, toggled from the right-click menu.
- **Multilingual** — Simplified Chinese / Traditional Chinese / English / Japanese.
- **Lightweight, permission-free** — no Accessibility, no private APIs.

### Install
1. Download `HideTray.dmg` from [Releases](https://github.com/bennix/macHideTray/releases/latest).
2. Open the DMG and drag **HideTray** into **Applications**.

### ⚠️ First launch (important)
This app is **not Apple-notarized**, so macOS blocks it on the **first** open after downloading with *"cannot be opened because Apple cannot check it for malicious software."* That is macOS's **standard Gatekeeper prompt for un-notarized apps — not a virus warning.** Do **one** of the following, **once**:

- **Option A (recommended):** In Applications, **right-click (Control-click) HideTray → Open → Open**. Double-click works normally afterward.
- **Option B:** Right-click → Open the `允许打开 Allow-Open.command` helper inside the DMG.
- **Option C:** Run in Terminal:
  ```bash
  xattr -dr com.apple.quarantine /Applications/HideTray.app
  ```

### Usage
- **Left-click** the toggle icon: expand / collapse hidden icons.
- **Right-click** the toggle icon: menu (launch at login, auto-collapse delay, language, quit).
- **Choose what gets hidden:** **⌘-drag** menu-bar icons to reorder them — icons to the **left** of the separator are hidden.

### Known limitation
Hiding granularity is "everything left of the separator," not per-icon. Use ⌘-drag to decide which icons fall into the hidden zone.

---

_Made with AppKit. Menu-bar icon hider, ~640 KB._
