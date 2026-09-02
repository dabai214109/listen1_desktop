# Listen 1 音乐播放器（桌面版）

> **仓库说明（fork 修改版）**
>
> 本仓库 fork 自 [listen1/listen1_desktop](https://github.com/listen1/listen1_desktop)，并非官方仓库。在此基础上做了以下修改：
>
> 1. **修复 bilibili 多 P 视频只播放第一 P 的问题**：播放合集类视频（如 200 首歌曲合集）时，播放队列会自动展开全部分 P，播完一 P 自动续播下一 P（修改 `app/listen1_chrome_extension/js/provider/bilibili.js` 与 `js/player_thread.js`）。
> 2. **支持粘贴 bilibili 视频链接导入歌单**：`www.bilibili.com/video/BVxxx`、裸 `BV` 号链接可导入为完整分 P 歌单（原来只支持 `/audio/am` 音频链接）。
> 3. **CI 调整**：GitHub Actions 只构建 Windows x64 安装包。
>
> 安装包在 Actions 产物或 Releases 中下载。上游官方版请移步 [listen1/listen1_desktop](https://github.com/listen1/listen1_desktop)。

Listen 1 可以搜索和播放来自多个主流音乐网站的歌曲，让你的曲库更全面。并支持收藏功能，方便的创建自己的歌单。

支持音乐平台

- 网易云音乐
- QQ 音乐
- 酷狗音乐
- 酷我音乐
- bilibili
- 咪咕音乐
- 千千音乐

[![imgur](http://i.imgur.com/Ae6ItmA.png)]()

- 支持 Windows，Mac，Linux 平台

# 安装方式

访问 github 主页下载安装包安装

网址：https://listen1.github.io/listen1

## 生成完整代码

项目中包含了 listen1_chrome_extension 的引用，在 checkout 后需要把引用库初始化

    git submodule update --init --recursive

## 运行

    npm run start

## 生成安装包

全平台安装包

    npm run dist

Windows 安装包

    npm run dist:win32
    npm run dist:win64

Mac 安装包

    npm run dist:mac

Linux 安装包

    npm run dist:linux32
    npm run dist:linux64
