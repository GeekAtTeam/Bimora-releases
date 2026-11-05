<p align="center">
  <img src="assets/icon.png" alt="Bimora" width="128" height="128">
</p>

<h1 align="center">Bimora</h1>

<p align="center">专注写作，即时呈现。</p>

Bimora 是一款简洁、离线可用的桌面 Markdown 编辑器。打开即可写作，文档保存在本地，无需登录。

由 [GeekAt](https://geekat.cn) 开发。本仓库用于发布安装包、记录版本更新和收集问题反馈，不包含应用源码。

## 下载

准备发布 **v0.1.0 公开预览版**，提供 Windows x64 和 Linux x64 安装包。

发布后，请前往 [下载页面](https://github.com/GeekAtTeam/Bimora-releases/releases) 展开对应版本的 **Assets**，选择适合系统的安装包：

| 系统 | 安装包 |
| --- | --- |
| Windows x64 | `Bimora-0.1.0-windows-x64-setup.exe` |
| Ubuntu / Debian x64 | `Bimora-0.1.0-linux-amd64.deb` |
| 其他 Linux x64 | `Bimora-0.1.0-linux-x86_64.AppImage` |

安装包自带运行环境，无需安装 Node.js。macOS 和 ARM64 版本暂未提供。

GitHub 自动生成的 `Source code (zip)` 和 `Source code (tar.gz)` 是本仓库的文档压缩包，不是应用安装包。

## 功能

- **打开即写**：新建、打开、保存和另存为本地 Markdown 文件。
- **双模式编辑**：默认即时渲染，可切换源码模式，支持查找和替换。
- **文件与大纲**：侧边栏浏览目录和文件，通过大纲跳转标题。
- **保存与恢复**：可选自动保存、草稿恢复及外部修改检测。
- **本地图片与外观**：插入本地图片，支持浅色、深色与跟随系统主题。

版本变化见 [更新日志](CHANGELOG.md)。

## 安装

### Windows

下载并运行 `.exe` 安装程序，按照向导完成安装。

v0.1.0 安装程序尚未签名，系统可能显示未知发布者提示；Windows 真机兼容性仍在持续验证。

### Ubuntu / Debian

在下载目录打开终端，执行：

```bash
sudo apt install ./Bimora-0.1.0-linux-amd64.deb
```

安装后从应用列表启动 Bimora。

### Linux AppImage

```bash
chmod +x Bimora-0.1.0-linux-x86_64.AppImage
./Bimora-0.1.0-linux-x86_64.AppImage
```

AppImage 需要系统具备相应的 FUSE 支持；Ubuntu / Debian 用户建议优先使用 `.deb`。

## 开始写作

启动后可直接输入，按 `Ctrl+S` 选择位置保存。已有文档可以通过“文件”菜单打开，也可以打开文件夹后从侧边栏选择文件。

| 操作 | 快捷键 |
| --- | --- |
| 新建文档 | `Ctrl+N` |
| 打开文件 | `Ctrl+O` |
| 保存 | `Ctrl+S` |
| 另存为 | `Ctrl+Shift+S` |
| 查找 / 替换 | `Ctrl+F` / `Ctrl+H` |
| 切换源码模式 | `Ctrl+/` |

这是首个公开预览版本，即时渲染与 Markdown 兼容性仍在完善。遇到不支持的语法时可使用源码模式编辑，重要文档建议保留备份。

当前版本暂不提供自动更新，请从下载页面获取后续版本。

## 问题反馈

欢迎在 [Issues](https://github.com/GeekAtTeam/Bimora-releases/issues) 提交问题或建议。请尽量附上系统版本、Bimora 版本、复现步骤；如涉及文档显示问题，可提供不含敏感信息的最小示例。

## 版权与第三方声明

Bimora 为闭源软件，应用源码不在本仓库公开。本仓库公开文档和提供安装包下载不表示将应用授予开源许可。

第三方组件遵循各自许可证，相关声明随安装包提供，包括 `THIRD_PARTY_NOTICES.txt` 及 Electron / Chromium 的许可文件。
