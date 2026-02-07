# 选择 IDE

在 [学习路线图](/技术栈/快速开始/学习路线图.md) 中提到了一些开发工具。本文将根据实际使用体验，介绍各种 IDE 的特点，帮助你选择适合自己的工具。

## 主流 IDE 对比

### Visual Studio Code（强烈推荐）

**适用语言**：JavaScript, TypeScript, Python, C++, Java, Go, PHP, Ruby 等

**优势：**
- ✅ 免费且开源，跨平台
- ✅ 丰富的插件生态系统，几乎支持所有语言
- ✅ 内置 Git 支持，强大的调试功能
- ✅ 轻量级，启动速度快
- ✅ 智能代码补全和提示
- ✅ 集成终端

**适用场景：**
- 前端开发（HTML/CSS/JavaScript）
- 全栈开发
- 数据科学（Python）
- 几乎所有编程语言

**推荐理由：**
VS Code 是目前最受欢迎的代码编辑器，支持几乎所有语言和框架。插件生态极其丰富，可以根据需要自由定制。编写这本 Wiki 使用的就是 VS Code。

### IntelliJ IDEA

**适用语言**：Java, Kotlin, Scala, Groovy

**优势：**
- ✅ 强大的代码智能提示和重构功能
- ✅ 集成版本控制系统
- ✅ 完善的插件生态
- ✅ 优秀的性能，适合大型项目

**适用场景：**
- Java 开发（首选）
- 企业级应用开发
- Spring 等框架开发

### PyCharm

**适用语言**：Python

**优势：**
- ✅ 专为 Python 设计，功能强大
- ✅ 代码分析和调试工具完善
- ✅ 集成 Django 和 Flask 框架
- ✅ 版本控制系统集成

**适用场景：**
- Python Web 开发
- 数据科学
- 机器学习

### Visual Studio

**适用语言**：C#, C++, Visual Basic, F#, JavaScript

**优势：**
- ✅ 功能强大，适合 Windows 应用开发
- ✅ 支持 Azure 集成
- ✅ 强大的调试和测试工具
- ✅ 适合大型项目

**适用场景：**
- C# 开发（首选）
- Windows 桌面应用
- .NET 开发
- 游戏开发（Unity）

### Sublime Text

**适用语言**：几乎所有编程语言

**优势：**
- ✅ 极快的启动和响应速度
- ✅ 强大的多光标编辑
- ✅ 丰富的包生态系统
- ✅ 轻量级

**适用场景：**
- 快速编辑文本和代码
- 追求效率的开发者
- 不喜欢复杂 IDE 的用户

### Android Studio

**适用语言**：Java, Kotlin

**优势：**
- ✅ 官方 Android 开发 IDE
- ✅ 强大的布局编辑器
- ✅ 集成模拟器
- ✅ 支持 Gradle 构建系统

**适用场景：**
- Android 应用开发
- 移动应用开发

## 按语言选择 IDE

### Python
- **VS Code** + Python 扩展（推荐新手）
- **PyCharm Community**（专业开发）
- **Jupyter Notebook**（数据分析）

### C/C++
- **VS Code** + C/C++ 扩展（推荐）
- **Visual Studio**（Windows，功能强大）
- **Dev-C++**（初学者，NOI/NOIP 等比赛指定工具）
- **Code::Blocks**（免费，跨平台）

### Java
- **IntelliJ IDEA**（首选，强烈推荐）
- **VS Code** + Java 扩展（轻量级）
- **Eclipse**（免费，经典但较老）

### JavaScript/TypeScript
- **VS Code**（首选，强烈推荐）
- **WebStorm**（JetBrains 出品，付费）

### Go
- **VS Code** + Go 扩展（推荐）
- **GoLand**（JetBrains 出品，付费）

### C#
- **Visual Studio**（首选）
- **VS Code** + C# 扩展
- **JetBrains Rider**（跨平台，付费）

## 按场景选择 IDE

### 新手学习编程
- **VS Code** - 轻量级，易上手
- **Thonny**（Python）
- **Dev-C++**（C语言）

### Web 前端开发
- **VS Code** - 绝对首选

### 企业级开发
- **IntelliJ IDEA**（Java）
- **Visual Studio**（C#）
- **PyCharm**（Python）

### 数据科学
- **Jupyter Notebook**（Python）
- **VS Code**（通用）
- **PyCharm**（Python）

### 算法竞赛
- **Dev-C++**（简单快速）
- **VS Code**（功能更强）
- **CLion**（付费，专业）

### 移动开发
- **Android Studio**（Android）
- **Xcode**（iOS，macOS 专有）

## 实用建议

### 可以同时安装多个 IDE 吗？

✅ 可以，但建议根据主要开发语言选择 1-2 个主 IDE

### 不同 IDE 之间会冲突吗？

⚠️ 可能会出现冲突，特别是：
- VS 和 VS Code 的 C++ 插件可能冲突
- 多个 IDE 占用大量磁盘空间

### 如何切换 IDE？

大部分 IDE 都可以导入项目，可以随时切换

## 我的推荐

### 计算机专业学生

```bash
主力 IDE: VS Code
备用 IDE:
  - Python → PyCharm
  - Java → IntelliJ IDEA
  - C++ → CLion 或 VS Code
```

### 初学者

```bash
Python: VS Code + Python 扩展
C/C++: Dev-C++（简单）或 VS Code（功能强）
```

### Web 开发者

```bash
首选: VS Code
```

### 为什么强烈推荐 VS Code？

1. **通用性** - 几乎支持所有语言
2. **免费** - 完全免费且开源
3. **插件丰富** - 想要什么功能都有插件
4. **轻量级** - 启动快，占用资源少
5. **社区活跃** - 大量的教程和问题解决方案
6. **持续更新** - 微软持续维护和改进

## 更多资源

- [工具软件简介 - OI Wiki](https://oi-wiki.org/tools/)
- [VS Code 官网](https://code.visualstudio.com/)
- [JetBrains IDE 介绍](https://www.jetbrains.com/zh-cn/ide/)

---

**总结**：对于大多数情况，VS Code 是最好的选择。当你有特殊需求时（如大型 Java 项目），再考虑专业 IDE。
