# frp-panel Android — 发行制品

本仓库**只存放公开发布的安装包与更新清单**，不包含 App 源码（源码仓库私有）。

## 下载

- 安装包：`https://github.com/Le0nByte/frp-panel-android-releases/releases/latest/download/frp-panel-android-<版本>.apk`
- 更新清单：`update-manifest.json` / `update-manifest.json.sig`

App 内置的公钥会校验 `update-manifest.json` 的 RSA 签名，并比对 APK 的
SHA-256、大小与签名证书指纹后才安装。**手工下载安装包时无法享受该校验**，
建议直接使用 App 内的「软件更新」功能。

## 校验下载（可选）

```bash
sha256sum frp-panel-android-<版本>.apk   # 与 update-manifest.json 中的 sha256 对比
```

## 兼容性

- 最低 Android 8.0（API 26）
- 升级安装要求同签名；跨签名版本需先卸载（会丢失本地保存的 Master 连接信息）
