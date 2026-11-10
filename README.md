# BallsHackPro-Releases

BallsHackPro 版本发布仓库 —— 存放**启动器安装包 / 全量更新包 / 增量更新清单**，用于官网直链下载与客户端自动更新分发。

## 版本规范

- 版本号：`vX.Y.Z`，与客户端 `version.json` 中的 `latest_version` 保持一致
- Git Tag：`vX.Y.Z`（Release 以 tag 为锚点）
- Release 标题：`vX.Y.Z`
- 必填产物：启动器安装包（Windows）；可选产物：全量更新包、增量清单

## 产物命名

| 产物 | 命名 | 说明 |
|---|---|---|
| 启动器 | `BallsHackPro-vX.Y.Z-setup.exe` | 官网「Windows 下载」直链 |
| 全量更新包 | `latest_full.zip` | 客户端整包更新（走 `/api/download`） |
| 增量清单 | `manifest.json` | 增量更新清单（文件列表 + MD5，走 `/api/update/manifest`） |

## 发布流程

```bash
# 1) 打 tag 并推送
git tag v1.4.8 && git push origin v1.4.8

# 2) 创建 Release 并上传产物（gh CLI）
gh release create v1.4.8 ./BallsHackPro-v1.4.8-setup.exe \
  --title "v1.4.8" --notes "更新说明：..."

# 3) 或网页操作：Releases → Draft a new release → 上传附件
```

## 客户端更新检查

客户端启动时请求 `https://api.solohomie.top/api/version`，服务端返回：

```json
{
  "latest_version": "1.4.8",
  "min_version": "1.4.8",
  "force_update": false,
  "download_url": "https://api.solohomie.top/api/download",
  "direct_download_url": "https://api.solohomie.top/api/download",
  "changelog": "更新说明"
}
```

客户端据此判断是否需要更新 / 静默更新；下载源可指向服务器 `/api/download`，也可改成指向本仓库的 Release 直链。

## 关联仓库

- 客户端源码：[SoloHomie/BallsHackPro](https://github.com/SoloHomie/BallsHackPro)
- 服务端源码：[SoloHomie/BallsHackProService](https://github.com/SoloHomie/BallsHackProService)
- 官网：`solohomie.top`（首页 + 下载页，部署在 154.64.252.204）
