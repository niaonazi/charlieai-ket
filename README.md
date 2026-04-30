# CharlieAI KET作文批改系统

这是一个可直接部署到 GitHub Pages 的静态 HTML 工具。

## 部署文件

- `index.html`：GitHub Pages 默认入口，内容与定稿 HTML 一致。
- `KET作文批改系统.html`：本地使用文件。
- `CharlieAI_KET作文批改系统_使用流程与功能说明.md`：老师使用说明。

## GitHub Pages 部署方式

1. 在 GitHub 新建一个仓库。
2. 把本文件夹内容推送到仓库。
3. 进入仓库 `Settings -> Pages`。
4. Source 选择 `Deploy from a branch`。
5. Branch 选择 `main`，目录选择 `/root`。
6. 保存后等待 GitHub Pages 发布。

发布后访问地址通常类似：

```text
https://你的用户名.github.io/仓库名/
```

## 用户数据怎么处理

系统里的班级、学生和批改结果默认保存在浏览器 `localStorage` 中，不会自动上传到 GitHub。

这意味着：

- 每位老师的数据只在自己的浏览器里。
- GitHub Pages 只托管网页代码，不保存学生数据。
- 从本地 `file://` 版本切换到 GitHub Pages 网址时，原浏览器缓存不会自动迁移。
- 以后只要 GitHub Pages 网址不变，更新 `index.html` 通常不会清空老师浏览器里的数据。

## 本地版迁移到 GitHub Pages

迁移步骤：

1. 在本地旧版本里点击左下角“备份”，下载 `CharlieAI_Backup_*.json`。
2. 打开 GitHub Pages 线上版本。
3. 点击左下角“恢复”，选择刚才的备份 JSON。
4. 确认班级和学生记录恢复成功。

## 隐私提醒

不要把 `CharlieAI_Backup_*.json`、Excel 导出表、家校反馈文本提交到 GitHub。

本仓库的 `.gitignore` 已经默认忽略这些本地数据文件。
