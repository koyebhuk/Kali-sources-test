# Kali源测试工具

本项目是一个用于测试多个 Kali Linux 镜像源状态、延迟和下载速度的网页工具。用户可以一键测试所有源，并根据测试结果选择最佳的更新源，同时支持一键复制源配置。

## 功能特性

- 支持一键测试多个 Kali 镜像源的可用性、延迟和下载速度
- 结果可按速度或延迟排序
- 自动推荐最佳源（延迟最低）
- 支持一键复制源配置到剪贴板
- 结果摘要与配置预览高亮显示
- 响应式设计，适配桌面与移动端

## 使用方法

1. 打开 [Kali-sources-test.html ]()文件（**可直接用浏览器打开，无需服务器环境**）。
2. 点击“开始测试所有源”按钮，等待测试完成。
3. 可根据需要点击“按速度排序”或“按延迟排序”按钮。
4. 推荐源和最佳配置会在测试完成后自动显示，也可在每个源卡片点击“复制配置”按钮获取对应配置。

## 复制配置功能

每个源卡片底部有两个按钮：
- **重新测试**：单独重新测试该源
- **复制配置**：生成该源的完整配置信息，例如：
```text
# 中科大: Kali滚动更新分支
deb http://mirrors.ustc.edu.cn/kali kali-rolling main non-free contrib 
deb-src http://mirrors.ustc.edu.cn/kali kali-rolling main non-free contrib
```

点击"复制配置"按钮后，配置信息会显示在页面底部的预览区域，您可以：

1. 直接阅读配置内容
2. 点击"复制配置"按钮将内容复制到剪贴板
3. 粘贴到您的Kali系统源配置文件（`/etc/apt/sources.list`）中

## 依赖

- [Font Awesome](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css)
	提供一套可缩放矢量图标库（SVG 图标），通过 CSS 即可调用，无需下载图片文件。
- [Google Fonts - Roboto](https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap)
	从 Google 服务器动态加载 Roboto 字体（由 Google 设计的现代无衬线字体）。

以上依赖均通过 CDN 自动加载，无需手动安装。

## 文件说明

- [`Kali-sources-test.html`]()：主页面及全部功能实现

## 截图

[界面截图]()

## 免责声明

本工具测试结果仅供参考，实际速度和可用性可能受网络环境影响。请定期测试以获得最佳体验。

---

如有建议或问题，欢迎提交 Issue 或 PR！