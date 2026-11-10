# BallsHackPro · 官方下载

**BallsHackPro** 是面向球宝的 Windows 桌面辅助工具：锁定目标、流畅合球、精准调控，游戏体验全面升级。

- 🌐 官网：<https://solohomie.top>
- 💬 Discord：<https://discord.gg/YtvJrFvcC5>

## 系统要求

| 项目 | 要求 |
|---|---|
| 系统 | Windows 10 / 11（64 位） |
| 运行环境 | MuMu 模拟器（前台运行，工具才生效） |
| 权限 | 建议以管理员身份运行 |

## 下载与安装

1. 打开 [Releases](https://github.com/SoloHomie/BallsHackPro-Releases/releases) 页面
2. 下载最新版本的 **启动器**（约 26 MB）
3. 运行安装包，按提示完成安装
4. 首次启动会自动下载完整客户端文件，请保持网络畅通

> 更早的版本可在 Releases 里翻历史记录；建议始终使用最新版。

## 使用要点

- 工具只在 MuMu 模拟器处于**前台**时生效，切到其他窗口即可正常打字
- 登录后在软件内完成订阅 / 兑换码开通
- 支持自动更新：新版本发布后客户端会提示，可静默更新

## 常见问题

**打不开 / 闪退？**
请确认 Windows 为 64 位、已安装最新启动器，并尝试以管理员身份运行；如仍无法启动，请到 Discord 反馈。

**杀毒软件报毒？**
游戏辅助类工具常被误报。可先添加信任目录；如不放心，请在沙箱环境或备用机运行，风险自担。

**订阅 / 兑换码问题？**
在软件内对应页面操作，或到 Discord 咨询管理员。

## 反馈

- Discord：<https://discord.gg/YtvJrFvcC5>
- 问题反馈：<https://github.com/SoloHomie/BallsHackPro-Public/issues>

---

## 维护者：发布流程

仅面向维护者，普通用户可忽略。

- 版本号：`vX.Y.Z`，与客户端 `version.json` 的 `latest_version` 对齐
- 产物命名：启动器 `BallsHackPro-vX.Y.Z-setup.exe`、全量包 `latest_full.zip`、增量清单 `manifest.json`

```bash
git tag v1.4.8 && git push origin v1.4.8
gh release create v1.4.8 ./BallsHackPro-v1.4.8-setup.exe \
  --title "v1.4.8" --notes "更新说明..."
```

客户端通过 `https://api.solohomie.top/api/version` 检查更新，按 `version.json` 的 `latest_version` / `min_version` 决定提示或强制更新；下载源默认走服务器 `/api/download`，也可改为本仓库 Release 直链。

## 关联仓库

- 客户端源码：[SoloHomie/BallsHackPro](https://github.com/SoloHomie/BallsHackPro)
- 服务端源码：[SoloHomie/BallsHackProService](https://github.com/SoloHomie/BallsHackProService)
