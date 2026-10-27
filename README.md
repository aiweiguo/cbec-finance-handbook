# 随州网·跨境电商 财务学习手册

单文件静态站点：根目录打开 `index.html` 即可。

## 本地预览

用浏览器直接打开 `index.html`，或：

```bash
python3 -m http.server 8765
```

然后访问 http://127.0.0.1:8765/

## 部署

线上：<https://cw.newdata.top>

静态文件在 VPS `152`（`43.228.86.35`）的 `/var/www/cw`，nginx 直接提供。DNS 保持 Cloudflare 灰云，证书由 certbot 签发，到期 2027-01-25，之后自动续期。

更新页面：

```bash
rsync -av index.html 152:/var/www/cw/index.html
```

检索日与证据说明见页面内「来源与证据」。
