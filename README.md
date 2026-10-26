# MyJiva

MyJiva 桌面应用的下载与更新页面。目前提供「项目协同」和「日报与汇报」两个模块。

**[下载最新版本](https://github.com/ttlb0814/personal-workspace-release/releases/latest)**

## 选择安装包

| 系统 | 文件名（以 1.0.0 为例） | 适合谁 |
| --- | --- | --- |
| Windows x64 · 便携版 | `MyJiva-1.0.0-Windows-x64.exe` | 下载后双击运行，不想安装的用户 |
| Windows x64 · 安装版 | `MyJiva-1.0.0-Windows-x64-Setup.exe` | 希望以后在应用内下载、安装更新的用户 |
| macOS · Apple 芯片 | `MyJiva-1.0.0-macOS-arm64.dmg` | 使用 Apple 芯片 Mac 的用户 |

进入最新版本页面后，下载与你的系统对应的**一个安装包**即可。后续版本的文件名会使用对应的新版本号。

`latest.yml` 和 `.blockmap` 是 Windows 安装版更新所需的文件，普通用户无需下载。

## 如何更新

- **Windows 安装版**：应用发现新版本后，可以在应用内下载；下载完成后，由你确认“安装并重启”。
- **Windows 便携版**：应用会提示新版本，点击后前往下载页，手动下载新版 EXE。
- **macOS 版**：应用会提示新版本，点击后前往下载页，手动下载新版 DMG。

只有发布了**高于当前版本号**的正式版本，应用才会提示更新。例如，正在使用 1.0.0 时，重新发布 1.0.0 不会触发更新。

## 安装提示

Windows 版本目前未使用 Authenticode 代码签名，系统可能显示发布者或安全提示。macOS 版本目前使用临时签名，未经 Apple 公证，首次打开时也可能出现系统安全提示。请只从本仓库的 Releases 页面下载安装包。

## 给发布者

发布 Windows 安装版时，请将同一次打包生成的以下三个文件上传到**同一个正式 Release**：

- `MyJiva-版本号-Windows-x64-Setup.exe`
- `MyJiva-版本号-Windows-x64-Setup.exe.blockmap`
- `latest.yml`

如同时发布 Windows 便携版和 macOS 版，再上传各自的 EXE、DMG。发布前确认版本号一致、所有文件上传完成，并将 Release 设为 **Latest**。不要重命名 Setup.exe，也不要手动修改 `latest.yml`。
