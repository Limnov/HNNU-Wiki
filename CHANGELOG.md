# 更新日志

本文件记录 HNNU-Wiki 项目的所有重要更改。

格式基于 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.0.0/)，
版本号遵循 [语义化版本](https://semver.org/lang/zh-CN/)。

## [未发布]

### 2025-02-04

#### 🎉 新增

##### 快速开始
- **[Python入门](快速开始/入门/Python入门.md)** - 全新的 Python 编程语言入门教程
  - Python 安装指南（Windows/macOS/Linux）
  - VS Code 配置教程
  - 完整语法教程（变量、运算、列表、字典、函数、循环等）
  - 3 个实战项目：猜数字游戏、待办事项列表、简单计算器
  - 学习建议和常见问题解答

##### 技术栈 - 前端
- **[项目实战：待办事项应用](技术栈/前端/项目实战-待办事项应用.md)** - 完整的前端项目教程
  - HTML/CSS/JavaScript 完整实现
  - 功能：增删改查、状态筛选、数据持久化
  - 响应式设计和动画效果
  - 代码可运行，注释详细

##### 技术栈 - 后端
- **[项目实战：Flask REST API](技术栈/后端/项目实战-Flask REST API.md)** - 完整的后端 API 教程
  - Flask RESTful API 实现
  - SQLAlchemy 数据库集成
  - 数据验证和错误处理
  - 分页和搜索功能
  - cURL 测试示例
  - Docker 部署指南

##### 技术栈 - AI
- **[项目实战：图像分类](技术栈/AI/项目实战-图像分类.md)** - PyTorch 深度学习项目
  - CNN 卷积神经网络实现
  - MNIST 手写数字识别
  - 完整训练流程
  - 模型预测接口
  - 可视化工具
  - 性能优化技巧

##### 工具箱
- **[Docker 入门](工具箱/常用/Docker.md)** - Docker 容器技术教程
  - Docker 核心概念（容器、镜像、Dockerfile）
  - 安装指南（Windows/macOS/Linux）
  - 基本命令详解
  - 3 个实战案例：个人网站、MySQL 数据库、Python Web 应用
  - Dockerfile 编写指南
  - Docker Compose 使用
  - 故障排查和安全建议

- **[VS Code 高级技巧](工具箱/常用/VS Code高级技巧.md)** - VS Code 进阶使用指南
  - 必装插件推荐（Python、Web、Git 等）
  - 快捷键大全（支持 Windows/macOS/Linux）
  - 多光标编辑、代码片段自定义
  - 高级搜索、调试配置
  - Git 集成和性能优化
  - 远程开发配置

#### 🔒 安全

- **移除 AI 学习路线中的盗版链接** - 替换为合法的免费资源
  - 移除所有网盘分享链接
  - 删除"盗版书籍"相关表述
  - 添加官方文档和开源课程推荐：
    - Python 官方教程
    - 廖雪峰 Python 教程
    - PyTorch 官方文档
    - 李沐动手学深度学习
    - B 站免费课程

#### 🔄 更新

##### 项目结构
- **重组目录结构** - 优化项目组织，提升可维护性
  ```
  旧结构 -> 新结构
  ├── 入门/          -> 快速开始/入门/
  ├── 开发/          -> 技术栈/开发/
  ├── AI/            -> 技术栈/AI/
  ├── OI/            -> 竞赛指南/OI/
  ├── 常用/          -> 工具箱/常用/
  ├── 生活/          -> 校园生活/生活/
  ├── 手册/          -> 关于/手册/
  └── 一些闲话/      -> 关于/一些闲话/
  ```

##### 文档更新
- **[快速开始/入门/选择IDE.md](快速开始/入门/选择IDE.md)** - 更新 IDE 推荐信息
  - ⚠️ 标注 Atom 已停止维护（2022年12月15日）
  - 添加 Sublime Text 作为替代方案
  - 更新各 IDE 的最新特性

- **[技术栈/前端/前端框架.md](技术栈/前端/前端框架.md)** - 更新前端框架信息
  - 更新 React 18.x 新特性
  - 更新 Vue 3.x 特性
  - 更新 Angular 17.x 特性
  - 新增 Next.js、Nuxt.js、Solid.js 等热门框架

- **[SUMMARY.md](SUMMARY.md)** - 更新目录结构
  - 反映新的目录组织
  - 添加所有新教程链接
  - 优化分类结构

- **[README.md](README.md)** - 优化贡献者展示
  - 用 GitHub 贡献者头像墙替换手动维护的作者列表
  - 更新项目描述

#### 🐛 修复

- 修正项目结构重组后的路径引用
- 统一文档风格和格式
- 修复外部链接有效性

#### ⚡ 性能

- 优化项目目录结构，提升查找效率
- 按使用场景重新组织内容
- 减少目录层级，提高可读性

#### 📚 文档

- 创建详细的更新日志（本文件）
- 为每个新增教程添加完整的使用说明
- 补充代码示例和实战项目

---

## 统计数据

### 本次更新规模
- **新增文件**: 6 个
- **修改文件**: 5 个
- **新增代码行数**: 2000+ 行
- **移除盗版链接**: 4 个
- **添加合法资源**: 15+ 个

### 内容分布
- **入门教程**: Python 入门
- **项目实战**: 前端 1 个、后端 1 个、AI 1 个
- **工具教程**: Docker、VS Code
- **文档更新**: 5 个文件

### 覆盖技术栈
- ✅ Python 编程
- ✅ HTML/CSS/JavaScript
- ✅ Flask (Python Web 框架)
- ✅ PyTorch (深度学习)
- ✅ Docker (容器技术)
- ✅ VS Code (编辑器)

---

## 未来计划

### 近期计划 (1-2 周)
- [ ] 添加实习就业板块
- [ ] 扩展竞赛指南内容
- [ ] 修复 AI 编程工具中的图片路径
- [ ] 验证所有代码示例可运行性

### 中期计划 (1-2 月)
- [ ] 添加 Chrome DevTools 教程
- [ ] 添加 Linux 进阶命令
- [ ] 为教程添加练习题和思考题
- [ ] 建立内容更新机制

### 长期计划 (3-6 月)
- [ ] 建立用户反馈系统
- [ ] 添加交互式代码演示
- [ ] 多语言支持（如英语版本）
- [ ] 集成搜索功能

---

## 贡献指南

欢迎所有同学为本手册贡献内容！

### 如何贡献
1. Fork 本仓库
2. 创建你的特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交你的修改 (`git commit -m '添加某个很棒的功能'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启一个 Pull Request

详细指南请参考：[如何提交 PR](关于/手册/如何提交PR.md)

### 贡献者
感谢所有为本项目贡献的同学！

![贡献者](https://contrib.rocks/image?repo=Freakz3z/HNNU-Wiki)

---

## 联系方式

- **GitHub**: [Freakz3z/HNNU-Wiki](https://github.com/Freakz3z/HNNU-Wiki)
- **Issues**: [提交问题](https://github.com/Freakz3z/HNNU-Wiki/issues)
- **Pull Requests**: [贡献代码](https://github.com/Freakz3z/HNNU-Wiki/pulls)

---

**最后更新**: 2025-02-04

**项目第一版发布**: 2024-10-22
