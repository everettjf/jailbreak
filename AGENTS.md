# 项目约定

- 这是一个 GitHub Pages + Jekyll（just-the-docs 主题）的 iOS 越狱教程文档站。
- 每次修改完成后，直接 `git add -A && git commit && git push origin main`，无需再逐次确认；推送后 GitHub Pages 自动构建部署。
- 提交信息使用英文，简短描述改动。
- 改动后先本地验证：`bundle install && bundle exec jekyll build` 通过再提交。

## 配图约定

- 每篇文章尽量配 1 张以上图片（截图优先）。
- 图片统一放 `assets/images/`，文件名用英文小写加连字符，如 `dopamine-home.png`。
- 引用方式：`![描述]({{ '/assets/images/xxx.png' | relative_url }})`，必须写有意义的 alt 描述。
- 截图尚未提供时，先用 HTML 注释占位（如 `<!-- 配图：xxx 截图 assets/images/xxx.png -->`），不要引用不存在的图片文件，避免线上裂图。
