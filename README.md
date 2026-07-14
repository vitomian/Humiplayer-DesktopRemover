<div align="center">

# 🎭 HumiPlayer

### 桌面创意摸鱼神器

**在桌面上挖个洞，安心摸鱼不被发现**


[快速开始](#-快速开始) • [功能特性](#-功能特性) • [使用说明](#-使用说明) • [技术栈](#-技术栈)

</div>

---

## ✨ 项目简介

HumiPlayer 是一款 Windows 桌面应用，通过**全屏透明覆盖 + 局部挖空**的方式，让你在公开环境下也能安心进行私密操作。

上班想摸鱼？看视频、玩游戏、处理私事？只需在桌面上挖几个洞，洞外区域全遮挡，洞内内容随便看，老板路过也不怕。

> 💡 灵感来源于「上班摸鱼」这一普遍职场现象——既然躲不掉，那就优雅地摸。

---

## 🎯 功能特性

### 🏗️ 场景搭建模式
- **多图层支持**：背景图片、图片图层、文字图层，自由组合场景
- **多种挖空形状**：矩形 / 圆角矩形 / 圆形 / 不规则洞形 / 五角星
- **自定义填色**：挖空区域支持自定义填充颜色和透明度
- **一键平铺**：上传图片自动适应画布，无需手动调整

### 🎮 场景运行模式
- **全屏透明覆盖**：遮挡整个屏幕，只露出挖空区域
- **穿透操作**：挖空区域可直接操作后方桌面内容
- **20 个快捷槽位**：最多支持 20 个挖空区域，每个可独立设置快捷键
- **一键切换**：快捷键即时显示/隐藏挖空区域

### 📚 新手教程引导
- **三步式引导**：上传图片 → 去图模式 → 运行场景，跟着走一遍就会
- **高亮提示**：实时高亮当前操作区域，不用找按钮
- **可跳过 / 不再提示**：支持跳过和关闭，自由控制

### ⚙️ 个性化设置
- **热键自定义**：20 个恢复快捷键自由配置（默认 Ctrl+1 ~ Ctrl+Shift+0）
- **深色主题**：半透明毛玻璃风格 UI，好看又不刺眼
- **场景保存**：支持保存/加载场景文件 (`.hscene`)

---

## 🚀 快速开始

### 直接安装（推荐）

从 [Releases](https://github.com/yourname/HumiPlayer/releases) 下载最新的 `HumiPlayer-Setup-v1.0.0.exe`，双击安装即可。

### 系统要求
- Windows 10 及以上
- .NET 8.0 运行时（独立部署包已内置，无需额外安装）

---

## 📖 使用说明

### 三步上手

**1️⃣ 上传图片**
- 进入场景搭建，点击「图片」按钮上传背景图
- 图片自动平铺适应画布

**2️⃣ 绘制挖空区域**
- 点击「去图模式」按钮
- 选择形状（矩形/圆形/五角星等）
- 在画布上拖动鼠标绘制挖空区域
- 可自定义填充颜色和透明度

**3️⃣ 运行场景**
- 点击「运行场景」按钮进入全屏模式
- 挖空区域可穿透操作桌面内容
- 按设置的快捷键显示/隐藏各个区域
- 按退出热键（默认 F12）退出运行模式

### 快捷键

| 功能 | 快捷键 |
|------|--------|
| 去图模式（运行中） | `Ctrl + Shift + R` |
| 恢复区域 1-10 | `Ctrl + 1` ~ `Ctrl + 0` |
| 恢复区域 11-20 | `Ctrl + Shift + 1` ~ `Ctrl + Shift + 0` |
| 退出运行模式 | `F12` |

> 所有快捷键均可在「设置」页面自定义

---

## 🛠️ 技术栈

| 类别 | 技术 |
|------|------|
| UI 框架 | [Avalonia UI 11.3](https://avaloniaui.net/) |
| 架构模式 | MVVM (Prism.Avalonia) |
| 图形渲染 | SkiaSharp + SixLabors.ImageSharp |
| 视频播放 | LibVLCSharp + FFmpeg |
| 主题 | Semi.Avalonia |
| 目标框架 | .NET 8.0 |
| 打包工具 | Inno Setup 6 |

### 项目结构

```
HumiPlayer/
├── Assets/                 # 静态资源（图标、图片）
├── Controls/               # 自定义控件
│   ├── SkiaCanvasControl   # Skia 画布控件
│   ├── TutorialOverlay     # 教程引导控件
│   └── VideoPlayerControl  # 视频播放控件
├── Models/                 # 数据模型
├── Services/               # 业务服务
│   ├── ImageProcessingService.cs
│   ├── UserPreferencesService.cs
│   └── MaterialLibraryService.cs
├── Utility/                # 工具类
│   ├── GlobalHotkeyManager.cs
│   └── ThemeManager.cs
├── ViewModels/             # 视图模型
├── Views/                  # 视图
│   ├── WelcomeView         # 欢迎页
│   ├── SceneBuilderView    # 场景搭建
│   ├── ScenePlayWindow     # 场景运行
│   └── SettingsView        # 设置页
└── HumiPlayer.csproj
```

---

## 🤝 参与贡献

欢迎提交 Issue 和 Pull Request！

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 打开 Pull Request

---

## 📄 许可证

本项目采用 MIT 许可证 - 详见 [LICENSE](LICENSE) 文件

---

<div align="center">

**如果觉得好用，别忘了点个 ⭐ Star 支持一下**

Made with ❤️ using [TRAE](https://trae.cn/)

</div>
