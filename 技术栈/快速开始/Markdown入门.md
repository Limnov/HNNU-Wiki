# Markdown 入门指南

## 什么是 Markdown？

Markdown 是一种轻量级标记语言，让你用纯文本格式编写文档，然后转换成 HTML。它简单易学，广泛用于 README、技术文档、博客等。

**为什么使用 Markdown？**
- ✅ 简单 - 10分钟掌握基础
- ✅ 通用 - GitHub、Reddit 等平台支持
- ✅ 高效 - 专注内容而非格式
- ✅ 兼容 - 可转换为 HTML、PDF 等

## 基础语法

### 标题

```markdown
# 一级标题
## 二级标题
### 三级标题
```

### 文本样式

```markdown
**粗体**
*斜体*
***粗斜体***
~~删除线~~
`行内代码`
```

**渲染效果：**
**粗体**
*斜体*
***粗斜体***
~~删除线~~
`行内代码`

### 列表

**无序列表：**
```markdown
- 项目 1
- 项目 2
  - 子项目 2.1
```

**有序列表：**
```markdown
1. 第一项
2. 第二项
```

**任务列表：**
```markdown
- [x] 已完成
- [ ] 未完成
```

**渲染效果：**
- 项目 1
- 项目 2
  - 子项目 2.1

1. 第一项
2. 第二项

- [x] 已完成
- [ ] 未完成

### 链接和图片

```markdown
[链接文本](https://example.com)

![图片描述](/image/logo.jpg)
```

### 引用

```markdown
> 这是一段引用
>
> > 嵌套引用
```

**渲染效果：**
> 这是一段引用
>
> > 嵌套引用

### 代码块

````markdown
```python
def hello():
    print("Hello, World!")
```
````

**渲染效果：**
```python
def hello():
    print("Hello, World!")
```

**常用语言标识：** `python`、`javascript`、`java`、`bash`、`html`、`css`、`json`

### 表格

```markdown
| 列1 | 列2 | 列3 |
|-----|-----|-----|
| 内容1 | 内容2 | 内容3 |

| 左对齐 | 居中 | 右对齐 |
|:-------|:----:|-------:|
| 内容   | 内容 | 内容   |
```

**渲染效果：**
| 列1 | 列2 | 列3 |
|-----|-----|-----|
| 内容1 | 内容2 | 内容3 |

| 左对齐 | 居中 | 右对齐 |
|:-------|:----:|-------:|
| 内容   | 内容 | 内容   |

### 分隔线

```markdown
---

***
```

**渲染效果：**
---

## 常用技巧

### 转义字符

使用反斜杠 `\` 转义特殊字符：

```markdown
\*不是斜体\*
```

### 换行

段落之间空一行，段落内行末加两个空格强制换行。

### HTML 支持

Markdown 支持 HTML 标签：

```markdown
<div style="color: red;">红色文字</div>
<br>  <!-- 换行 -->
```

## GitHub 特有语法

### 任务列表

```markdown
- [ ] 待办事项
- [x] 已完成
```

### 代码块语法高亮

GitHub 自动识别语言并高亮：

````markdown
```python
def hello():
    print("Hello")
```
````

### 自动链接

URL 自动转换为链接：

```markdown
https://github.com/
```

## VS Code 快捷键

| 功能 | Windows/Linux | macOS |
|------|---------------|-------|
| 粗体 | Ctrl+B | Cmd+B |
| 斜体 | Ctrl+I | Cmd+I |
| 切换预览 | Ctrl+Shift+V | Cmd+Shift+V |
| 侧边预览 | Ctrl+K V | Cmd+K V |

## 推荐工具

### 编辑器

- **VS Code** + Markdown All in One 扩展
- **Typora** - 所见即所得
- **Obsidian** - 知识管理

### 在线编辑

- [StackEdit](https://stackedit.io/) - 在线编辑器
- [Markdown Live Preview](https://markdown-it.github.io/) - 实时预览

## 最佳实践

### 文档结构

```markdown
# 标题

## 主要章节

### 子章节

- 使用列表组织内容
- 代码块指定语言
```

### 命名规范

- 文件名：`README.md`、`api-guide.md`
- 使用小写字母和连字符
- 标题简短明确

### 图片管理

```markdown
<!-- 使用相对路径 -->
![图片](./images/screenshot.png)

<!-- 统一放在 image/ 目录 -->
![图片](/image/logo.jpg)
```

### 代码示例

```markdown
## 安装

\`\`\`bash
npm install
\`\`\`

## 使用

\`\`\`javascript
const app = require('./app')
\`\`\`
```

## 速查表

| 功能 | 语法 |
|------|------|
| 粗体 | `**text**` |
| 斜体 | `*text*` |
| 标题 | `# Title` |
| 链接 | `[text](url)` |
| 图片 | `![alt](url)` |
| 代码 | `` `code` `` |
| 代码块 | ` ``` ` |
| 列表 | `- item` |
| 引用 | `> quote` |
| 表格 | `\| col \|` |
| 删除线 | `~~text~~` |

## 学习资源

- [Markdown 官方教程](https://www.markdowntutorial.com/)
- [GitHub Flavored Markdown](https://github.github.com/gfm/)
- [Mastering Markdown - GitHub](https://guides.github.com/features/mastering-markdown/)

---

**记住**：Markdown 的核心是简单。掌握基础语法就够用了！
