# 使用指南

本页面介绍如何使用本项目，以及如何通过 Git、MkDocs 和 GitHub Actions 完成文档的修改、构建与部署。

## 1. 项目使用流程

本项目采用 Markdown 编写文档，并通过 MkDocs Material 生成静态网站。完成修改后，将代码推送到 GitHub，即可触发自动化部署。

具体操作步骤如下：

### 第一步：修改文档

在本地项目的 `docs/` 目录中找到需要修改的 Markdown 文件。

例如：

- `index.md`：修改网站首页。
- `about.md`：修改项目介绍。
- `guide.md`：修改使用指南。
- `api.md`：修改 API 参考。

使用 Typora 编辑并保存文件。

### 第二步：本地预览

打开 CMD，进入项目根目录，启动 MkDocs 本地预览服务：

```bash
py -3.12 -m mkdocs serve
```

然后在浏览器中访问：

`http://127.0.0.1:8000/`

检查页面内容、导航菜单、表格和超链接是否正常。

### 第三步：提交并推送修改

确认文档没有问题后，使用 Git 管理修改。

```bash
# 查看文件修改状态
git status

# 将修改加入暂存区
git add docs/

# 查看暂存区中的修改
git diff --staged

# 创建一次版本提交
git commit -m "更新技术文档"

# 推送到 GitHub 的 main 分支
git push origin main
```

### 第四步：检查自动构建与部署

打开 GitHub 仓库，进入 Actions 页面。

找到名为 `Deploy MkDocs to GitHub Pages` 的工作流，检查构建和部署任务是否成功。

如果出现错误，可以点击失败的任务，查看详细日志。

### 第五步：访问网站

部署成功后，打开 GitHub Pages 网站。

检查修改后的内容是否已经显示在网站上，确认导航链接和页面布局正常。

## 2. 常用命令参考

在项目开发过程中，经常需要使用以下命令：

| 命令                                | 作用                     |
| ----------------------------------- | ------------------------ |
| `git status`                        | 查看当前文件修改状态     |
| `git add`                           | 将修改加入暂存区         |
| `git commit`                        | 创建本地版本记录         |
| `git push`                          | 将本地提交推送到远程仓库 |
| `git pull`                          | 获取并合并远程仓库的更新 |
| `git log`                           | 查看历史提交记录         |
| `py -3.12 -m mkdocs serve`          | 启动本地预览             |
| `py -3.12 -m mkdocs build --strict` | 构建网站并严格检查警告   |

## 3. Git 基本工作原理

Git 的日常开发流程主要分为三个阶段：

1. 工作区：修改项目中的文件。
2. 暂存区：使用 `git add` 选择需要提交的修改。
3. 本地仓库：使用 `git commit` 保存版本记录。

最后通过 `git push` 将本地提交上传到 GitHub 远程仓库。

例如：

```bash
git add docs/guide.md
git commit -m "完善使用指南"
git push origin main
```

需要注意，`git commit` 只是将修改保存到本地 Git 仓库，并不会自动上传到 GitHub。

## 4. 注意事项

- 修改文档后，应先进行本地预览。
- 提交之前使用 `git status` 检查修改内容。
- 不要将 Python 虚拟环境和自动生成的 `site/` 目录提交到 GitHub。
- 推送代码后，应检查 GitHub Actions 的运行结果。
- 如果网站没有立即更新，可以稍等片刻后刷新浏览器。

## 5. 实践体会

通过本次实践，我逐渐理解了 Git 工作区、暂存区和本地仓库之间的关系，也认识到 Git 不仅可以保存代码，还可以帮助开发者追踪项目的修改历史。

同时，MkDocs 和 GitHub Actions 将文档编写、网站构建与自动部署联系起来，使得修改 Markdown 文件后，可以通过一次 Git 推送完成网站更新。

## 6. 相关页面

- [返回首页](index.md)
- [关于本项目](about.md)
- [API 参考](api.md)