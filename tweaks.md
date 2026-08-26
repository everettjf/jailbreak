---
layout: default
title: 插件清单
parent: 设备与插件
nav_order: 2
---

这里列出我在各台越狱设备上安装和使用的插件 (Tweaks)。

## iPhone XR — iOS 16.1.1（Dopamine Rootless）

<!-- 配图：已装插件主界面截图，如 Filza / NewTerm / Choicy 设置页 assets/images/xr-tweaks-filza.png -->

| 插件名 | 功能 | 源 | 状态 | 官网 / 教程 | 使用说明 |
|--------|------|-----|------|-------------|----------|
| **Filza** | 文件管理器 | `https://tigisoftware.com/repo/` | ✅ 已装 | [官网](https://www.tigisoftware.com/) / [指南](https://www.tigisoftware.com/default/?p=439) | 浏览 `/var/jb` 查看越狱文件；查看 App 包内容路径为 `/var/containers/Bundle/Application/`；长按文件可分享或修改权限 |
| **NewTerm** | 终端工具 | `https://repo.chariz.com/` | ✅ 已装 | [Chariz](https://chariz.com/get/newterm3) / [GitHub](https://github.com/hbang/NewTerm) | 输入 `frida-server --version` 检查版本；ps aux \| grep frida 查看进程；`sudo killall frida-server` 重启服务；`su` 后密码默认 `alpine` |
| **CCSupport** | 控制中心模块支持 | `https://opa334.github.io/` | ✅ 已装 | [GitHub](https://github.com/opa334/CCSupport) | 安装后无需配置，作为底层依赖供其他 CC 插件调用；在「设置 → 控制中心」可管理第三方模块 |
| **Frida** | 动态插桩/JS 注入 | `https://build.frida.re` | ✅ 已装 | [官方文档](https://frida.re/docs/ios/) | PC 端执行 `frida-ps -U` 列进程；`frida -U -f com.bundle.id` 启动注入；`frida -U com.bundle.id` 附加运行中进程；确保设备端 `frida-server` 已运行 |
| **Choicy** | 禁用特定 App 的 tweak 注入 | `https://opa334.github.io/` | ✅ 已装 | [GitHub](https://github.com/opa334/Choicy) | 打开「设置 → Choicy」，选择目标 App → 开启「Disable Tweak Injection」；Frida 调试某 App 频繁崩溃时，先用 Choicy 禁用该 App 的所有 tweak 注入，排除冲突 |
| **iCleaner Pro** | 系统清理优化 | `https://ib-soft.net/cydia/` | ⬜ 未装 | [官网](https://ib-soft.net/) | 打开 App → 分析 → 清理缓存/日志/临时文件；「+」号页可管理 Launch Daemons 和 Cydia 源；排查 tweak 冲突时，可用它临时禁用部分插件 |
| **AppData** | 长按图标查看应用数据 | `https://fouadraheb.com/` | ⬜ 未装 | [官网](https://fouadraheb.com/) / [GitHub](https://github.com/FouadRaheb) | 桌面长按任意 App 图标 → 点击「AppData」→ 直接复制 Bundle ID、沙盒路径、容器路径；配合 Frida 时直接粘贴 Bundle ID 到 PC 命令行 |
| **RealCC** | 真正关闭 Wi-Fi/蓝牙 | BigBoss（自带） | ⬜ 未装 | [BigBoss](https://cydia.saurik.com/package/com.muirey03.realcc/) | 安装即生效；控制中心点击 Wi-Fi/蓝牙图标会**真正断开**而非仅断开当前网络；再次点击恢复 |
| **CopyLog** | 剪贴板历史 | `https://havoc.app/` | ⬜ 未装 | [Havoc](https://havoc.app/package/copylog) | 安装后键盘上方会出现剪贴板条；点击历史记录直接粘贴；支持搜索和收藏常用文本；复制 Frida 命令或 Bundle ID 后自动保存历史 |
| **Atria** | 桌面布局自定义 | `https://repo.chariz.com/` | ⬜ 未装 | [Chariz](https://chariz.com/get/atria) / [GitHub](https://github.com/ren7995/Atria) | 桌面空白处长按进入编辑模式 → 点击「Atria」按钮；可调整行列数、图标间距、Dock 数量；设置完成后点击 Respring 生效 |

### 小结

已装好 **5 个核心插件**（Filza、NewTerm、CCSupport、Frida、Choicy），覆盖了文件管理、终端操作、Frida 注入、冲突排查的全部基础需求。

接下来优先安装 **AppData**（配合 Frida 获取 Bundle ID 极方便）和 **iCleaner Pro**（系统维护/排错）。

## iPhone 11 — iOS 26.0.1（Dopamine）

> 📝 待补充

## iPhone 14 — iOS 17.3.1（Dopamine / RELAXIN）

> 📝 待补充
