# Git 入门指南

## 为什么需要 Git？

Git 是分布式版本控制系统，是程序员必备技能：

- ✅ **版本控制** - 记录每次修改，随时回退
- ✅ **团队协作** - 多人开发同一项目
- ✅ **代码备份** - 远程仓库托管代码
- ✅ **分支管理** - 独立开发功能，互不影响
- ✅ **开源贡献** - GitHub 上的项目都用 Git

**真实场景：**
- ❌ 没有 Git：`代码_final.py`、`代码_final2.py`、`代码_真的final.py`
- ✅ 有 Git：清晰的版本历史，随时回退

## 安装 Git

### Windows
1. 访问 [Git官网](https://git-scm.com/downloads)
2. 下载 Windows 安装包
3. 安装时建议选择 VS Code 作为默认编辑器
4. 验证：`git --version`

### macOS

```bash
brew install git
# 或
xcode-select --install
```

### Linux

```bash
sudo apt install git  # Ubuntu/Debian
```

## 初始配置

安装完成后，配置用户信息：

```bash
git config --global user.name "你的名字"
git config --global user.email "your.email@example.com"
git config --global init.defaultBranch main
```

## Git 基础概念

### 三个区域

```
工作区（Working）   →   暂存区（Stage）   →   本地仓库（Repository）
    你的文件               准备提交的            已提交的内容
```

### 工作流程

```
1. 修改文件
   ↓
2. git add（添加到暂存区）
   ↓
3. git commit（提交到本地仓库）
   ↓
4. git push（推送到远程仓库）
```

## 基础命令

### 创建仓库

```bash
# 初始化新仓库
git init

# 克隆远程仓库
git clone https://github.com/username/repo.git
```

### 查看状态

```bash
git status           # 查看仓库状态
git diff             # 查看文件修改内容
git log              # 查看提交历史
git log --oneline    # 简洁的日志显示
```

### 添加和提交

```bash
# 添加文件到暂存区
git add filename.py

# 添加所有修改的文件
git add .

# 提交暂存区的修改
git commit -m "提交说明"

# 添加并提交（一步完成）
git commit -am "提交说明"
```

**提交信息规范：**
```bash
git commit -m "feat: 添加用户登录功能"
git commit -m "fix: 修复密码验证bug"
git commit -m "docs: 更新README文档"
```

### 查看和回退

```bash
# 回退到指定版本（保留工作区修改）
git reset --soft HEAD~1

# 回退到指定版本（丢弃所有修改）⚠️
git reset --hard HEAD~1

# 恢复某个文件到指定版本
git checkout HEAD~1 filename.py
```

## 分支管理

### 为什么需要分支？

- 多人协作互不影响
- 开发新功能不破坏主代码
- 易于实验和尝试

### 分支命令

```bash
# 查看所有分支
git branch

# 创建并切换到新分支
git checkout -b feature-login

# 切换回主分支
git checkout main

# 合并分支
git merge feature-login

# 删除已合并的分支
git branch -d feature-login
```

### 实战：功能开发流程

```bash
# 1. 从主分支创建功能分支
git checkout main
git checkout -b feature-add-login

# 2. 在功能分支上开发
echo "登录功能代码" > login.py
git add login.py
git commit -m "feat: 添加用户登录功能"

# 3. 切换回主分支
git checkout main

# 4. 合并功能分支
git merge feature-add-login

# 5. 删除功能分支
git branch -d feature-add-login
```

## 远程仓库（GitHub）

### 创建远程仓库

**GitHub：**
1. 访问 [GitHub](https://github.com/)
2. 点击 "+" → "New repository"
3. 填写仓库名称、描述
4. 点击 "Create repository"

### 连接远程仓库

```bash
# 添加远程仓库
git remote add origin https://github.com/username/repo.git

# 查看远程仓库
git remote -v

# 推送到远程仓库
git push -u origin main

# 拉取远程更新
git pull
```

### 完整工作流程

```bash
# 1. 克隆仓库
git clone https://github.com/username/repo.git
cd repo

# 2. 创建功能分支
git checkout -b feature-new

# 3. 修改文件
echo "新功能" > new_feature.py

# 4. 提交修改
git add new_feature.py
git commit -m "feat: 添加新功能"

# 5. 推送到远程
git push -u origin feature-new

# 6. 在 GitHub 上创建 Pull Request

# 7. 合并后更新主分支
git checkout main
git pull origin main
```

## 常见场景

### 修改了最后一个提交

```bash
# 修改最后一次提交信息
git commit --amend -m "正确的提交信息"
```

### 暂存当前工作

```bash
# 临时切换分支
git stash

# 切换到其他分支工作
git checkout other-branch

# 完成后恢复
git checkout main
git stash pop
```

### 撤销文件的修改

```bash
# 撤销工作区的修改
git restore filename.py
```

## 忽略文件

创建 `.gitignore` 文件：

```gitignore
# Python
__pycache__/
*.py[cod]
*$py.class
venv/
env/

# IDE
.vscode/
.idea/

# 系统文件
.DS_Store
Thumbs.db

# 项目特定
config.py
*.log
.env
```

## 最佳实践

### 提交规范

```bash
feat: 新功能
fix: 修复bug
docs: 文档修改
style: 代码格式
refactor: 重构
test: 添加测试
chore: 构建过程或辅助工具的变动
```

### 分支管理

```bash
main        # 生产环境
develop     # 开发环境
feature/xxx # 新功能
bugfix/xxx  # bug修复
hotfix/xxx  # 紧急修复
```

### 安全建议

1. **不要提交敏感信息**（密码、API密钥）
2. **定期备份**（推送到远程仓库）
3. **使用强密码和2FA**

## 常见问题

### Git 和 GitHub 有什么区别？

- **Git**：版本控制工具（软件）
- **GitHub**：代码托管平台（网站）
- 关系：类似 Word 和 Google Docs

### merge 和 rebase 有什么区别？

- `merge`：保留完整历史，有合并提交
- `rebase`：线性历史，更清晰
- 建议：本地用 rebase，远程用 merge

### 如何撤销一次错误的提交？

```bash
# 未推送到远程
git reset --hard HEAD~1

# 已推送到远程（危险！）
git reset --hard HEAD~1
git push -f  # 强制推送
```

## 学习资源

- [Git 官方文档](https://git-scm.com/doc)
- [Pro Git 中文版](https://git-scm.com/book/zh/v2)
- [廖雪峰 Git 教程](https://www.liaoxuefeng.com/wiki/896043488029600)
- [Learn Git Branching](https://learngitbranching.js.org/)（交互式教程）

---

**最后提醒**：
- 💡 多用 `git status` 查看状态
- 🎯 提交信息要清晰
- 📚 定期推送到远程备份
- 🚀 不要害怕用 Git，大胆尝试！

祝你 Git 学习愉快！🎉
