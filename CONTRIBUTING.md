# 贡献指南

欢迎您对 JadeView 项目做出贡献！我们非常感谢社区的支持和帮助。在贡献之前，请仔细阅读本指南，以确保您的贡献能够顺利被接受。

## 开发环境搭建

### 1. 安装 Rust
JadeView 是基于 Rust 开发的，因此您需要安装 Rust 开发环境。

```bash
# 安装 Rust
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

# 验证安装
rustc --version
cargo --version
```

### 2. 安装依赖

#### Windows 依赖
在 Windows 上，您需要安装以下依赖：

- [Visual Studio Build Tools](https://visualstudio.microsoft.com/zh-hans/downloads/#build-tools-for-visual-studio-2022)
- [WebView2 Runtime](https://developer.microsoft.com/en-us/microsoft-edge/webview2/#download-section)

### 3. 克隆仓库

```bash
git clone https://github.com/JadeViewDocs/library.git
cd library
```

### 4. 构建项目

```bash
# 构建 Debug 版本
cargo build

# 构建 Release 版本
cargo build --release
```

## 代码规范

### 1. Rust 代码规范
- 遵循 [Rust 官方代码风格指南](https://doc.rust-lang.org/nightly/style-guide/index.html)
- 使用 `rustfmt` 格式化代码
- 使用 `clippy` 检查代码质量

```bash
# 格式化代码
cargo fmt

# 检查代码质量
cargo clippy
```

### 2. C 代码规范
- 遵循 C99 标准
- 使用 4 个空格缩进
- 函数和变量命名使用下划线分隔（snake_case）
- 宏定义使用全大写字母，下划线分隔

### 3. 易语言代码规范
- 遵循易语言官方代码风格
- 变量命名使用中文或拼音
- 函数命名清晰明了，包含功能描述
- 添加必要的注释

## 提交 PR 的流程

### 1. Fork 仓库
在 GitHub 上 Fork 本仓库到您自己的账号下。

### 2. 创建分支

```bash
# 创建并切换到新分支
git checkout -b feature/your-feature-name
```

分支命名规范：
- 功能开发：`feature/feature-name`
- Bug 修复：`fix/bug-description`
- 文档更新：`docs/documentation-update`

### 3. 提交代码

```bash
# 添加修改的文件
git add .

# 提交代码
# 提交信息格式：<类型>: <描述>
git commit -m "feat: add new feature"
```

提交信息类型：
- `feat`: 新功能
- `fix`: Bug 修复
- `docs`: 文档更新
- `style`: 代码风格修改
- `refactor`: 代码重构
- `test`: 测试相关
- `chore`: 构建或工具相关

### 4. 推送分支

```bash
git push origin feature/your-feature-name
```

### 5. 创建 Pull Request
在 GitHub 上创建 Pull Request，描述您的修改内容、动机和预期效果。

## 测试要求

### 1. 单元测试
- 为新功能添加单元测试
- 确保现有测试通过

```bash
# 运行单元测试
cargo test
```

### 2. 集成测试
- 测试功能在实际环境中的表现
- 测试跨平台兼容性（Windows x86 和 x64）

### 3. 示例测试
- 更新或添加示例代码，展示新功能的使用方法
- 确保示例代码能够正常运行

## 问题反馈

如果您在开发过程中遇到问题，可以通过以下方式反馈：

1. 在 GitHub 上创建 [Issue](https://github.com/JadeViewDocs/library/issues)
2. 加入我们的 QQ 群：[pL3Lo2kAgg](https://qm.qq.com/q/pL3Lo2kAgg)
3. 查看 [文档](https://jade.run/)

## 行为准则

请遵守以下行为准则：

- 尊重他人，友好交流
- 接受建设性批评
- 关注社区利益
- 保持专业性

## 许可证

通过贡献代码，您同意您的贡献将被授权为 [MIT 许可证](LICENSE)。

感谢您的贡献！