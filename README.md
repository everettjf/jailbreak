# jailbreak

我的 iOS 越狱手册（GitHub Pages + Jekyll，just-the-docs 文档库主题）：记录越狱设备、工具（Dopamine / RELAXIN）、教程与插件 (Tweaks) 玩法。

## 章节结构

- `index.md` — 前言：设备总览与导读
- `concepts.md` — 越狱基础（概念扫盲，待补充）
- `inventory.md` — 设备与插件（父章节）
  - `devices.md` — 我的设备（iPhone XR / 11 / 14 / 17 Pro）
  - `tweaks.md` — 插件清单（占位模板，待补充实际插件）
- `tools.md` — 越狱工具（Dopamine、RELAXIN）
- `guides.md` + `guides/` — 越狱教程（Dopamine 篇 / RELAXIN 篇，待补充）
- `faq.md` — 常见问题（待补充）

## 部署

仓库 Settings → Pages → Source 选择 `main` 分支根目录，GitHub 自动用 Jekyll 构建发布。主题通过 `remote_theme` 加载，无需 GitHub Actions。

## 本地预览（可选）

```sh
bundle install
bundle exec jekyll serve
```

浏览器打开 http://localhost:4000 预览。
