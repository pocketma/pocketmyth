# POCKET MYTH 官网

纯静态站点（HTML + CSS + 原生 JS，无构建步骤），域名 `https://www.pocketmyth.net`。

## 目录

```
index.html      简体中文首页（PC + 移动两套 DOM）
en/             英文首页、英文资讯 /en/news/、兑换码页 /en/codes/
zh-tw/ ko/ vi/  各语言首页 + 资讯索引 + 3 个分类页 + 兑换码页 + 10 篇本地攻略
view/           活动落地页
articleHtml/    133 篇简体中文资讯
css/ js/ img/ jq/ layui/ swiper/   静态资源
404.html  robots.txt  sitemap.xml  vercel.json
```

## 本地预览

```bash
python -m http.server 8080
# 打开 http://localhost:8080/
```

## 部署到 Vercel

1. 推送本目录到 GitHub（`.gitignore`、`.vercelignore` 这类隐藏文件也要）；
2. Vercel → Add New Project → 导入仓库；
3. Framework Preset 选 **Other**，Build Command / Output Directory 都留空；
4. Deploy 后在 Settings → Domains 绑定 `www.pocketmyth.net`；
5. 到 Google Search Console / Bing Webmaster Tools 提交 `https://www.pocketmyth.net/sitemap.xml`。

`vercel.json` 已配置：目录 URL 强制 `/` 结尾，图片 / CSS / JS 带长缓存头。

## 说明

- 所有页面使用相对路径引用资源，放在根目录或任意子目录都能跑；
- 下载按钮指向游戏发行方落地页（`hk.qu06.cn`），换渠道时全站搜索替换；
- 站点纯静态，无后端、无用户数据。
