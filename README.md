# 我的技术文档

这是《开源软件构建技术理论与实践》的个人实践项目。网站使用 MkDocs Material 构建，并通过 GitHub Actions 发布到 GitHub Pages。

- [公开网站](https://3524967016ylj-jpg.github.io/my-docs/)
- [个人实验报告](report/README.md)
- [自动部署记录](https://github.com/3524967016ylj-jpg/my-docs/actions)

## 本地预览

使用 Python 3.12，在项目根目录运行：

```bash
python -m venv .venv
python -m pip install -r requirements.txt
python -m mkdocs serve
```

Windows 激活虚拟环境后再运行 `python` 命令；具体激活方式取决于终端。预览地址以命令输出为准。严格构建命令为 `python -m mkdocs build --strict`。

网站源文件位于 `docs/`；`site/` 是生成结果，已被 Git 忽略。部署工作流位于 `.github/workflows/deploy.yml`。
