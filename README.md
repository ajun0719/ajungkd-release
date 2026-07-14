# ajungkd

> 一款专为 GKD（开屏跳过）设计的 Android 快照分析与规则管理工具

![Android](https://img.shields.io/badge/Android-7.0%2B-brightgreen.svg)
![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Version](https://img.shields.io/badge/Version-1.0.0-orange.svg)

## 📖 项目简介

**ajungkd** 是一款 Android 应用，旨在帮助 GKD 用户快速分析和生成跳过广告的规则。它能够解析 GKD 生成的快照文件，直观地查看界面节点树，并一键生成符合 GKD 规范的订阅规则。

### 核心功能

- 🔍 **快照解析**：支持解析 GKD 生成的 `.zip` 和 `.json` 快照文件，自动提取节点树和截图。
- 🖱️ **截图点选节点**：点击快照截图上的任意控件，自动定位并选中对应的节点。
- 🎯 **智能选择器生成**：自动生成节点的选择器，支持上下文链（无 ID 时自动包含父级路径）。
- ✨ **高亮反馈**：选中的节点在截图上自动高亮框显示，交互直观。
- 📋 **复制/导出规则**：一键复制选择器或导出完整的订阅 JSON。
- 💾 **保存到订阅**：将选中的节点规则一键保存到你的远程订阅中，自动匹配应用包名。
- 📦 **远程订阅管理**：查看、添加、删除远程订阅，支持从 GitHub 拉取最新规则。
- ☁️ **上传到 GitHub**：将本地修改的订阅上传到 GitHub，自动管理版本号和提交备注。
- 📱 **添加应用**：从手机已安装应用列表中选择，快速添加到订阅。
- 📝 **规则组管理**：增删改查规则组，支持批量导入 JSON5 格式的规则。
- 📤 **分享接收**：支持从 GKD 直接分享快照到本应用，自动解析。


### 部分软件界面

<img width="1910" height="810" alt="image" src="https://github.com/user-attachments/assets/504e42e0-26e6-41a7-bb32-ec966419dec8" />



### 简易使用教程（详细版请前往微信公众号：52瞎折腾）：

1、可以直接在GKD快照页面选择快照，点击“分享到其他应用”，选择“ajungkd”，软件就会自动解析快照

<img width="869" height="926" alt="image" src="https://github.com/user-attachments/assets/c48eb543-d268-4194-9de5-ac898345d32c" />


2、软件解析快照后会显示相应的快照截图，在截图中点击你要生成规则的按钮或界面（会有高亮框提示），然后往下滑，软件会显示节点信息和节点列表

点击“导出订阅”，会自动复制当前选定区域的 GKD应用规则，可直接粘贴到GKD应用规则处导入 或者 粘贴在本app[规则管理页面]的[批量导入规则组],最后提交会保存在你的订阅中

点击“保存到订阅”，会自动识别应用并保存在你的订阅地址中

点击“管理远程订阅”，可以管理你的git订阅地址（目前仅测试了github）

<img width="865" height="925" alt="image" src="https://github.com/user-attachments/assets/f6f1675b-1f81-4936-a7b9-d5215ea4a03a" />



## 🛠️ 技术栈

- **语言**：Java
- **最低 SDK**：Android 7.0 (API 24)
- **构建工具**：Gradle
- **网络请求**：OkHttp
- **JSON 解析**：Gson
- **UI 组件**：Material Design Components, RecyclerView, CardView

## 📦 安装与运行

### 方式一：直接安装 APK

1. 从 [Releases](https://github.com/ajun0719/ajungkd-release/releases) 下载最新的 APK 文件。
2. 在手机上安装（需要允许安装未知来源应用）。
3. 打开应用，授予存储权限。

### 方式二：从源码构建(暂不提供源码)

```bash
# 克隆项目
git clone https://github.com/ajun0719/xxxxxx.git

# 进入项目目录
cd ajungkd-release

# 使用 Gradle 构建 debug 版本
./gradlew assembleDebug

# 安装到设备
./gradlew installDebug
