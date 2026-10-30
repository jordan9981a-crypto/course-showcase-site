# 全电技术课程 AI 实践成果展示平台

这是一个纯静态的中文课程作品展示网站，使用 HTML、CSS、原生 JavaScript 和 JSON 构建。

## 添加新学生作品

1. 将学生网站 HTML 文件放入 `works/学年/group编号/`，每个学生网站保持独立。
2. 将作品首页截图放入 `assets/covers/`，建议使用清晰的 PNG 或 JPG 图片。
3. 在 `data/projects.json` 中新增一条项目记录，填写 `year`、`group`、`title`、`members`、`keywords`、`description`、`date`、`url`、`cover`、`category` 和 `featured`。
4. 确认 `url` 和 `cover` 使用相对路径，例如 `works/2026/group03/index.html` 和 `assets/covers/2026-group03.png`。

## 添加新学年

在 `data/projects.json` 中使用新的四位数字学年，并在 `index.html` 的学年导航和对应学年区块中补充入口。没有作品的学年会显示“科研实践成果”。

## 替换封面图片

用新图片替换 `assets/covers/` 中对应文件，保持 JSON 里的 `cover` 路径和文件名一致。建议保留统一的图片比例，避免卡片高度变化。

## 静态部署

将整个 `course_showcase_site` 目录上传到 GitHub Pages、学校服务器或其他静态托管服务，入口文件是 `index.html`。本地预览可在该目录运行：

```text
python -m http.server 8088
```

然后打开 `http://127.0.0.1:8088/`。

## 重要说明

不要把学生 HTML 文件合并到 `index.html`。每个小组网站必须保持独立，避免不同作品之间发生 CSS 和 JavaScript 冲突。
