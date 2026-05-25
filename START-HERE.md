# Photo Frame App

这是从本地重新独立上传的 Photo Frame 项目备份，不再放在 `interesting` 项目里。

完整项目已经打包成 base64 分片，位置在 `archive-parts/`。

解开后会得到：

- `PhotoFrameApp/`：SwiftUI iOS App + WidgetKit 小组件尝试
- `photo-widget-pwa/`：网页/PWA 版本原型
- `scriptable-photo-frame/`：Scriptable 免费小组件方案

## 在 Mac 上恢复

```bash
git clone https://github.com/cherry123455/photo-frame-app.git
cd photo-frame-app
cat archive-parts/photo-frame-experiments-20260525.tar.gz.b64.part-* > photo-frame-experiments-20260525.tar.gz.b64
base64 -d -i photo-frame-experiments-20260525.tar.gz.b64 -o photo-frame-experiments-20260525.tar.gz
shasum -a 256 photo-frame-experiments-20260525.tar.gz
tar -xzf photo-frame-experiments-20260525.tar.gz
```

正确的压缩包 SHA256：

```text
ac5fba0e1dd5db3b086605d0e82156904ae427cb6f440d07fb1257205d3241c3
```

这个包不包含你的私人照片，也没有包含 Xcode 的本地构建缓存 `DerivedData`。