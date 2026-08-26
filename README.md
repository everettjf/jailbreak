# jailbreak

我的 iOS 越狱笔记站点（GitHub Pages + Jekyll）：记录越狱设备、工具（Dopamine / RELAXIN）与插件 (Tweaks) 玩法。

## 页面结构

- `index.md` — 首页，设备总览与导航
- `devices.md` — 设备列表（iPhone XR / 11 / 14 / 17 Pro）
- `tools.md` — 越狱工具介绍（Dopamine、RELAXIN）
- `tweaks.md` — 插件清单（当前为占位模板，待补充实际插件）

## 部署

仓库 Settings → Pages → Source 选择分支（如 `main`）和根目录 `/`，保存后 GitHub 会自动用 Jekyll 构建并发布。

## 本地预览（可选）

```sh
gem install bundler jekyll
jekyll serve
```

浏览器打开 http://localhost:4000 预览。
