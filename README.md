 V13 FVTT Seamless Video Loader Patch (FVTT 无缝视频加载屏补丁)
让你的 Foundry VTT 告别加载时的黑屏等待，实现 0 延迟的沉浸式进入体验。 


📖 简介 (Introduction)

传统的 FVTT 模组（Modules）需要在核心框架加载完毕后才能运行，这导致在点击“进入游戏”和加载界面出现之间，玩家会看到几秒钟的黑屏或灰色背景。

本项目不是一个常规模组，而是一段针对 FVTT 核心文件 (game.hbs) 的代码补丁。通过将视频硬编码（Hardcode）到游戏的主 HTML 模板中，我们可以实现：

🚀 0 延迟启动：浏览器渲染页面的瞬间视频即刻播放。

📺 绝对全屏：无视 UI 缩放设置，强制铺满 100vw / 100vh。

🔄 无缝衔接：消除从登录界面到地图加载之间的视觉断层。

✨ 特性 (Features)
即时播放：利用 HTML5 <video> 标签的原生加载速度，快于任何 JS 脚本。

沉浸式覆盖：自动隐藏原版 Loading 界面的背景、边框和阴影。

UI 适配：为原版加载进度条（Loading Bar）添加了动态文字描边，确保在亮色或暗色视频背景下均清晰可见。

轻量级：仅需修改一段 HTML/CSS，不增加额外的脚本负担。

🛠️ 安装指南 (Installation Guide)
⚠️ 警告：本补丁涉及修改 FVTT 核心文件。请在操作前备份相关文件！FVTT 更新后此修改会被覆盖，需要重新应用。

1. 准备视频素材
将你的 .webm 背景视频放入该目录。

默认路径："Data\modules\my-custom-loader\background.webm"

2. 定位核心文件
找到你的 FVTT 安装目录（非 User Data 目录）。

目标文件："App\resources\app\templates\views\game.hbs"


3. 应用补丁
将该文件替换即可

4. 重启 FVTT
保存文件并完全重启 Foundry VTT 客户端/服务端以生效。

❓ 常见问题 (FAQ)
Q: 为什么更新 FVTT 后失效了？

A: FVTT 更新会重置 resources/app 目录。你需要重新应用此补丁。建议保留一份修改好的 game.hbs 备份。

Q: 视频只有声音没有画面？

A: 确保视频路径正确。如果是在本地托管，请检查文件权限。

Q: 为什么一定要修改核心文件？用模组不行吗？

A: 模组加载太晚了。只有修改核心文件才能消除进入游戏瞬间的那一秒“黑色空窗期”。



## ⚖️ License & Attribution (许可与声明)

This project is licensed under the **GNU General Public License v3.0 (GPLv3)**.
本项目采用 **GNU GPLv3** 许可证。

You are free to use, modify, and distribute this patch, provided that:
1. You **must credit the original author** (YourName) in your fork or derived work.
2. If you distribute a modified version, it **must remain open-source** under the GPLv3 license.
3. This is a modification of core Foundry VTT files; original code rights belong to Foundry Gaming LLC.

**关于署名 (About Attribution):**
如果您在其整合包或教程中使用了本补丁，请务必保留原作者署名。
