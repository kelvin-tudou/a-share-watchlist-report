# V6.6B Deploy Status And Plan

## Current Status

- public_url: https://kelvin-tudou.github.io/a-share-watchlist-report/
- package_complete: yes
- upload_scope: `index.html`, `manifest.json`, `assets/`, `data/`
- local_absolute_paths: no expected
- token/sqlite/cache/private machine config: must be absent

## Option A: GitHub Pages

适合公开展示。新建只放静态报告的公开仓库，或使用 `gh-pages` 分支，仅上传 deploy-ready 目录内容。不要上传 token、SQLite、缓存、源码私密配置。成本低，访问方便，通常不需要绑定域名。

## Option B: Cloudflare Pages

适合静态站点。可以绑定 Git 仓库，也可以 Direct Upload 静态目录。成本低，访问速度较好，可后续绑定域名。上传前只选择 deploy-ready 目录。

## Option C: 本地临时分享

在 deploy-ready 目录运行本地静态服务器，例如 `python -m http.server 8080`，同一局域网朋友可通过本机 IP 访问。只适合短期同网络访问，不是公网发布。

## User Confirmation Needed

发布到公网前需要确认：选择平台、是否公开仓库、是否允许上传静态报告数据。
