# JadeView 动态库

JadeView 是一个基于 Rust 开发的 WebView 窗口库，提供 C 语言兼容的 API 接口，方便在其他语言（如易语言）中调用和使用。

## 🌟 主要功能

- **跨平台支持**：支持 Windows x86 和 x64 平台
- **现代化 WebView**：基于 wry 库，提供现代化的 Web 浏览体验
- **灵活的窗口管理**：支持创建、关闭、最大化、最小化等窗口操作
- **丰富的事件系统**：提供多种事件类型和回调机制
- **主题管理**：支持 Light、Dark、System 主题切换
- **背景材料**：支持 Mica、MicaAlt、Acrylic 背景效果
- **本地服务器**：内置本地服务器功能，支持自定义协议
- **安全的内存管理**：严格的内存管理机制，避免内存泄漏
- **易语言友好**：提供易语言调用示例和文档

## 📋 支持平台

- **Windows x86**：32位 Windows 系统
- **Windows x64**：64位 Windows 系统

## 📦 下载与安装

### 预编译版本

从 [Releases](https://github.com/JadeViewDocs/library/releases) 页面下载最新的预编译动态库：

### 包含文件

每个预编译包包含以下文件：

| 文件名 | 说明 |
|--------|------|
| `JadeView_x86.dll` | x86 平台主动态库 |
| `JadeView_x86.pdb` | x86 平台调试信息 |
| `JadeView.dll_x86.lib` | x86 平台导入库 |
| `JadeView.dll_x86.exp` | x86 平台导出符号 |
| `JadeView_x64.dll` | x64 平台主动态库 |
| `JadeView_x64.pdb` | x64 平台调试信息 |
| `JadeView.dll_x64.lib` | x64 平台导入库 |
| `JadeView.dll_x64.exp` | x64 平台导出符号 |
| `demo.e` | 易语言调用示例 |
| `JadeView.e` | 易语言SDK |


## 📚 API文档

完整的 API 文档位于 `docs` 目录下，包含以下内容：

- **核心API**：初始化、消息循环、清理等基础功能
- **窗口管理API**：创建、关闭窗口等操作
- **窗口属性API**：设置标题、大小、位置等
- **窗口状态API**：最小化、最大化、置顶等
- **WebView API**：导航、执行JavaScript等
- **事件系统API**：注册、注销事件处理器
- **主题API**：设置主题、背景材料等
- **IPC通信API**：发送、接收IPC消息
- **本地服务器API**：创建本地服务器
- **数据结构定义**：RGBA、WebViewSettings等


## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

---

**JadeView** - 让 WebView 开发更简单！
