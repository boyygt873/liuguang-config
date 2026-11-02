# liuguang-config

流光下载 App 的云端配方热更新配置与 APK 分发仓库。

## 链路

| 用途 | 地址 |
|---|---|
| 配方主源（App 内烧定） | https://cdn.jsdelivr.net/gh/boyygt873/liuguang-config@master/config.json |
| 配方备源 | https://raw.githubusercontent.com/boyygt873/liuguang-config/master/config.json |
| APK 分发 | https://cdn.jsdelivr.net/gh/boyygt873/liuguang-config@v<版本>/apk/app-release.apk |

## 更新流程

1. 改 `config.json` → 提交 master
2. 刷新 jsDelivr 缓存：`curl https://purge.jsdelivr.net/gh/boyygt873/liuguang-config@master/config.json`
3. 新版本发 APK：提交 `apk/app-release.apk` 并打 tag `v<版本>`，同步更新 `latest_version` 段
