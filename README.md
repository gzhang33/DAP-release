# DAP-release

Chint DAP 桌面端的更新清单仓库。**只放 `version.json`，不放源码，也不放安装包。**

客户端启动时匿名读取本仓库的 `version.json`，比对自己的版本号；发现新版本则弹出提示并打开飞书发布表格，由用户自行下载安装包。

```json
{
  "version": "1.0.0",
  "release_page": "https://chintsso.feishu.cn/base/...",
  "platforms": [{ "platform": "windows", "filename": "...", "sha256": "...", "size_bytes": 0, "format": "exe" }]
}
```

发布新版本时，在本仓库对 `version.json` 执行一次替换提交即可；安装包与发布说明在飞书表格维护，不进入本仓库。
