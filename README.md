<p align="center">
  <img src="assets/icon.png" alt="Bimora" width="128" height="128">
</p>

<h1 align="center">Bimora</h1>

<p align="center">专注写作，即时呈现。</p>

Bimora 是一款简洁、离线可用的桌面 Markdown 编辑器。打开即可写作，文档保存在本地，无需登录。

由 [GeekAt](https://geekat.cn) 开发。本仓库用于发布安装包、记录版本更新和收集问题反馈，不包含应用源码。

## 下载

准备发布 **v0.3.0 公开预览版**，提供 Windows x64 和 Linux x64 安装包。

发布后，请前往 [下载页面](https://github.com/GeekAtTeam/Bimora-releases/releases) 展开对应版本的 **Assets**，选择适合系统的安装包：

| 系统 | 安装包 |
| --- | --- |
| Windows x64 | `Bimora-0.3.0-windows-x64-setup.exe` |
| Ubuntu / Debian x64 | `Bimora-0.3.0-linux-amd64.deb` |
| 其他 Linux x64 | `Bimora-0.3.0-linux-x86_64.AppImage` |
| 下载校验 | `SHA256SUMS` |

安装包自带运行环境，无需安装 Node.js。macOS 和 ARM64 版本暂未提供。

GitHub 自动生成的 `Source code (zip)` 和 `Source code (tar.gz)` 是本仓库的文档压缩包，不是应用安装包。

## 功能

- **打开即写**：默认即时渲染，可切换源码模式；支持查找替换、多窗口和命令行打开文件。
- **文件与大纲**：目录浏览、快速打开、最近文件与目录、侧栏右键菜单，大纲跟随当前阅读章节。
- **扩展语法**：支持 YAML Front Matter、常用 HTML、数学公式、Mermaid、提示框、上下标和高亮；未支持的语法尽量在原处显示源码，其他正文继续渲染。
- **代码块与表格**：代码高亮、行号、一键复制及自动换行；表格支持尺寸调整、列对齐、行列操作和边界“+”快速插入。
- **图片与链接**：支持本地图片、图注、图片居中和逐图尺寸，点击链接可直接编辑 Markdown 语法。
- **保存与阅读**：可选自动保存、关闭窗口自动保存、手动恢复草稿和外部修改检测；切换模式或退出偏好设置时保留阅读位置。
- **多款主题**：提供 Light、Dark、GitHub、Newsprint、Night、Pixyll、Whitey，以及玄墨、宣纸及各自的柔和版、沧海、青瓷，共十三款内置主题，并记住所选主题。
- **导入与导出**：支持 HTML、PDF、PNG、打印和公众号样式复制；通过可选 Pandoc 导入 Word、LaTeX 等文档，或导出 Word、EPUB 等格式。
- **跨平台文本**：LF、CRLF 和混合换行均可直接渲染编辑，尽量保留文件原有的换行格式。

版本变化见 [更新日志](CHANGELOG.md)。

## 安装

### Windows

下载并运行 `.exe` 安装程序，按照向导完成安装。

v0.3.0 安装程序尚未签名，系统可能显示未知发布者提示；Windows 真机兼容性仍在持续验证。

### Ubuntu / Debian

在下载目录打开终端，执行：

```bash
sudo apt install ./Bimora-0.3.0-linux-amd64.deb
```

安装后从应用列表启动 Bimora。

### Linux AppImage

```bash
chmod +x Bimora-0.3.0-linux-x86_64.AppImage
./Bimora-0.3.0-linux-x86_64.AppImage
```

AppImage 需要系统具备相应的 FUSE 支持；Ubuntu / Debian 用户建议优先使用 `.deb`。当前 AppImage 启动器存在关闭 Chromium 沙箱的路径，需要该保护时请使用 `.deb`。

### 下载校验

将安装包和同一版本的 `SHA256SUMS` 下载到同一目录。Linux 可执行：

```bash
sha256sum --ignore-missing -c SHA256SUMS
```

Windows 可使用 PowerShell 计算校验值，与 `SHA256SUMS` 中对应文件的值比较：

```powershell
Get-FileHash .\Bimora-0.3.0-windows-x64-setup.exe -Algorithm SHA256
```

## 开始写作

启动后可直接输入，按 `Ctrl+S` 选择位置保存。已有文档可以通过“文件”菜单打开，也可以打开文件夹后从侧边栏选择文件。

| 操作 | 快捷键 |
| --- | --- |
| 新建文档 | `Ctrl+N` |
| 新建窗口 | `Ctrl+Shift+N` |
| 打开文件 | `Ctrl+O` |
| 快速打开 | `Ctrl+P` |
| 保存 | `Ctrl+S` |
| 另存为 | `Ctrl+Shift+S` |
| 查找 / 替换 | `Ctrl+F` / `Ctrl+H` |
| 切换源码模式 | `Ctrl+/` |

### 命令行

```bash
bimora                    # 新建空白窗口
bimora ./docs             # 新建窗口并打开目录
bimora ./docs/README.md   # 打开文件及其所在目录
bimora ./scripts/test.sh  # 以文本形式打开其他 UTF-8 文件
```

DEB 安装后可直接使用 `bimora`；Windows 安装后需新开终端。AppImage 可直接执行 `./Bimora-0.3.0-linux-x86_64.AppImage ./docs`，默认不添加 `bimora` 命令。

### 升级

关闭 Bimora 后安装新版。已选择的主题和偏好设置继续保留；v0.3.0 支持直接渲染 CRLF 和混合换行文件，无需手动转换格式或修改 Git 配置。

从 v0.1.0 升级时，主题改为记住所选项，不再随系统变化自动切换；启动时不再弹出草稿恢复列表，异常退出后的草稿可从“偏好设置 → 通用 → 保存 & 恢复 → 恢复未保存的草稿”查看。

正常关闭窗口时会保存当前文件的更改；未命名文档需先选择保存位置，取消保存或保存失败时保留窗口。

v0.3.0 仍为公开预览版本，即时渲染与 Markdown 兼容性仍在完善。重要文档建议保留备份。

当前版本暂不提供自动更新，请从下载页面获取后续版本。

### 导入、导出与公众号排版

“文件 → 导出”提供 HTML、无样式 HTML、PDF、PNG、打印与公众号排版。公众号排版可预览并复制带样式的文章，粘贴到微信公众号编辑器后请检查图片、链接和公式；此功能不会登录账号或自动发布文章。

导入 Word（DOCX）、LaTeX、reStructuredText、org-mode、Wiki、EPUB、Textile、OPML，以及导出 Word、EPUB 等格式，需要另行安装 [Pandoc](https://pandoc.org/installing.html)。可在“偏好设置 → 导出 → 通用”指定 Pandoc 路径。复杂排版转换后请检查结果，旧版 `.doc` 文件应先另存为 `.docx`。

## 问题反馈

欢迎在 [Issues](https://github.com/GeekAtTeam/Bimora-releases/issues) 提交问题或建议。请尽量附上系统版本、Bimora 版本、复现步骤；如涉及文档显示问题，可提供不含敏感信息的最小示例。

## 版权与第三方声明

Bimora 为闭源软件，应用源码不在本仓库公开。本仓库公开文档和提供安装包下载不表示将应用授予开源许可。

第三方组件遵循各自许可证，相关声明随安装包提供，包括 `THIRD_PARTY_NOTICES.txt` 及 Electron / Chromium 的许可文件。
