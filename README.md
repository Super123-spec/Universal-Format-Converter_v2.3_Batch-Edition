# 万能格式转换器 v2.3 批量版

Windows 桌面端的一站式格式转换工具。图纸、Office 文档、PDF、视频、音频、图片六大类格式集中在同一个界面里转换，支持拖拽批量处理，无需安装任何运行时或额外组件。

> **本仓库只放说明文档。程序本体体积较大（178 MB），请到 [Releases](../../releases) 页面下载。**

## 下载

前往 [Releases](../../releases) 页面，下载 `Universal-Format-Converter_v2.3_Batch.zip`（177 MB），解压后双击 `万能格式转换器.exe` 即可运行。

无需安装，DWG 引擎与 ffmpeg 已打包进程序内部。

## 支持的转换

| 类别 | 输入 | 输出 |
|---|---|---|
| 图纸 | DWG / DXF | PDF |
| 文档 | DOCX / DOC | PDF、TXT，docx ↔ doc 互转 |
| 表格 | XLSX / XLS | PDF、CSV，xlsx ↔ xls 互转 |
| 演示 | PPTX / PPT | PDF，pptx ↔ ppt 互转 |
| 文本 | CSV → XLSX，TXT → DOCX | |
| PDF | PDF | DOCX、XLSX、PPTX、PNG、JPG、TXT、DXF |
| 视频 | MKV / MOV / AVI / FLV / WEBM / WMV / M4V / TS | MP4、MP3、GIF |
| 音频 | FLAC / WAV / M4A / AAC / OGG / WMA / MP3 | MP3、WAV、M4A、FLAC |
| 图片 | HEIC / HEIF / PNG / JPG / WEBP / BMP / GIF / TIF / ICO / PPM / TGA | 任意其他图片格式 |

图片格式之间是全互通的；DWG / DXF 转 PDF 开箱即用，不需要额外装 CAD 软件。

## 使用方式

1. 双击 `万能格式转换器.exe`，等待 6~8 秒出现窗口
2. 把文件拖进窗口，或点「添加文件」/「添加文件夹」（会扫描子文件夹）
3. 在「转换为」列确认目标格式
4. 点「开始转换」

输出文件默认生成在原文件旁边，不会覆盖原文件，重名会自动加 `(1)`。

### 批量处理

- 「批量：全部设为」选一个目标格式 → 「应用到全部」，不支持的文件会自动跳过并记录在日志里
- 也可以选中若干行（Ctrl+A 全选、Ctrl+点击多选），用「选中行转成」单独设置
- 每个文件的目标格式可以各不相同
- 转换过程中点「取消」，会在当前文件结束后停止

详细说明见仓库内的 [使用说明.txt](使用说明.txt)。

## 系统要求

- Windows 10 / 11（64 位）
- 无需安装 Python、Office 或 CAD 软件

## 开源组件声明

本程序使用了以下开源组件，相应的许可证文本见 [开源声明-LibreDWG-GPLv3.txt](开源声明-LibreDWG-GPLv3.txt)：

- **LibreDWG** — GNU GPLv3，用于 DWG / DXF 解析
- **FFmpeg** — 用于音视频转码

关于 GPLv3 组件的源码获取方式，见 Releases 页面的说明。

## 反馈

使用中遇到问题，欢迎提 Issue，请附上转换前后的文件类型和日志输出。
