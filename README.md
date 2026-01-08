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

从 [Releases](https://github.com/yourusername/JadeView/releases) 页面下载最新的预编译动态库：

- `JadeView-dist_all_platforms.zip`：包含所有平台的动态库
- `JadeView-dist_x86.zip`：仅包含 x86 平台动态库
- `JadeView-dist_x64.zip`：仅包含 x64 平台动态库

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

## 🚀 快速开始

### 易语言调用示例

```e
.版本 2
.支持库 spec

.程序集 程序集1
.程序集变量 窗口设置, JadeView窗口设置
.程序集变量 JadeView, JadeView
.程序集变量 窗口id, 整数型

.子程序 _启动子程序, 整数型, , 本子程序在程序启动后最先执行
    创建测试窗口 ()
    返回 (0)  ' 可以根据您的需要返回任意数值

.子程序 创建测试窗口
.局部变量 JadeRady, 逻辑型
.局部变量 载入url, 文本型
.局部变量 服务目录, 文本型
.局部变量 开启DevTools, 逻辑型

    开启DevTools ＝ 是否为调试版 ()
    JadeRady ＝ JadeView.初始化 (开启DevTools, GBK文本到UTF8文本 (取运行目录 ()))
    
    .如果真 (JadeRady)
        服务目录 ＝ 取运行目录 () ＋ "\web"
        载入url ＝ JadeView创建本地服务 (GBK文本到UTF8文本 (服务目录), "jadeDemo")
        
        窗口设置.可调整大小边框 ＝ 真
        窗口设置.去除标题栏 ＝ 真
        窗口设置.高度 ＝ 620
        窗口设置.宽度 ＝ 530
        窗口设置.使用页面图标 ＝ 真
        
        窗口id ＝ JadeView.创建窗口 (载入url, 0, 窗口设置)
        .如果真 (窗口id ＞ 0)
            JadeView消息循环 ()
        .如果真结束
    .如果真结束
```

### C语言调用示例

```c
#include <stdio.h>
#include "JadeView.h"

int main() {
    // 初始化JadeView
    int success = JadeView_init(1, NULL, NULL);
    if (success) {
        printf("JadeView初始化成功\n");
        
        // 创建WebView窗口
        WebViewWindowOptions options = {
            .width = 800,
            .height = 600,
            .resizable = 1
        };
        
        uint32_t window_id = create_webview_window("https://www.example.com", 0, &options, NULL);
        if (window_id > 0) {
            printf("窗口创建成功，ID: %u\n", window_id);
            
            // 运行消息循环
            run_message_loop();
        }
    } else {
        printf("JadeView初始化失败\n");
    }
    
    return 0;
}
```

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