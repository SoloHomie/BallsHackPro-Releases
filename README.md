# BallsHackPro · 发行版

BallsHackPro 是一款面向 **MuMu 模拟器 12** 的球球大作战辅助客户端（Windows）。

- 官网与文档：<https://solohomie.top>
- Discord：<https://discord.gg/YtvJrFvcC5>

本仓库只存放**发行版安装包与更新说明**，源代码不公开。

## 系统要求

| 项目 | 要求 |
| --- | --- |
| 操作系统 | Windows 10 / 11 64 位 |
| 模拟器 | MuMu 模拟器 12（`MuMuVMMHeadless.exe` / `MuMuNxDevice.exe`） |
| 分辨率 | 横屏 16:9，建议 `1920x1080` |
| 运行权限 | 普通用户即可；部分环境需管理员权限才能读取进程 |

## 下载与安装

1. 从 [Releases](../../releases) 下载最新安装包，或访问官网「下载与安装」页面
2. 关闭游戏与模拟器后运行安装包
3. 启动客户端 → 登录 → 先进入对局，再点「重新检测」连接模拟器

安装与连接细节见文档：<https://solohomie.top/manual/newbie.html>

## 自动更新

客户端内置自动更新，流程为：

1. 启动时请求 `version.json`
2. 下载安装包并校验 **SHA-256**
3. 校验 **RSA 签名**（签名不匹配会直接拒绝）
4. 后台安装，下次启动生效

任一环节失败都不会影响当前版本使用，详情会写入错误中心（`Ctrl+Shift+E` 可复制）。

## 反馈问题

提交问题时请附上：

- 客户端版本（主界面右下角）
- 系统版本（`winver`）
- 日志目录 `logs\`（整个文件夹）
- 错误中心复制出的完整内容（`Ctrl+Shift+E`）

常见问题先查：<https://solohomie.top/manual/faq.html>

## 说明

本工具仅供学习与交流使用。使用前请确认你所在环境的相关规定，因使用本工具产生的一切后果由使用者自行承担。
