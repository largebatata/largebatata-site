# largebatata-site
Personal website for LargeBatata

## 网站

LargeBatata 的个人网站 V1。纯 HTML + CSS，没有 JavaScript、第三方字体、追踪脚本或运行依赖。支持手机、桌面和系统深浅色模式。

## 文件

```text
public/
  index.html    首页
  styles.css    共用样式与响应式布局
  favicon.svg   网站图标
  404.html      页面未找到
  _headers      Cloudflare Pages 响应头
  robots.txt    搜索引擎抓取规则
```

只将 `public/` 部署到网站。README 和本地工具不作为网页发布。

## Cloudflare Pages

正式访问地址：<https://largebatata.pages.dev>。已于 2026-10-01 部署到 Cloudflare Pages。

| 设置 | 值 |
| --- | --- |
| 项目名称 | `largebatata` |
| Git 仓库 | `largebatata/largebatata-site` |
| 生产分支 | `main` |
| Framework preset | `None` |
| Build command | 留空（无需构建） |
| Build output directory | `public` |
| Root directory | 仓库根目录，保留默认 |
| 环境变量、Functions、数据库 | 无 |
| 付费服务、Web Analytics | 不启用 |

选择 Pages 的 Git 集成，main 更新后自动部署。仅授权此仓库；GitHub/Cloudflare 登录、2FA 和安装授权由仓库所有者本人确认。

## 修改与扩展

- 修改首页内容：`public/index.html`。
- 修改颜色、排版：`public/styles.css` 的 CSS 变量和规则。
- 增加文字、照片、音乐、项目：有真实内容后，再在 `main` 中增加语义化 `section` 或独立 HTML 页面，并添加相应导航。
- 图片等静态文件可以放在 `public/assets/`；目前不创建空目录或占位内容。
- 为所有页面引用同一份样式。无需安装 npm 包；可使用任意本地静态 HTTP 服务器预览 `public/`。
- 提交到 main 后，在 Cloudflare 确认部署成功，再检查正式地址。

## 成本与以后绑定域名

当前只使用 GitHub 公开仓库和 Cloudflare Pages 免费计划，固定成本为每月 0、每年 0。未购买域名或套餐。免费服务条款及额度以供应商当时公布为准。

以后确认购买 `largebatata.com` 后，将域名添加到 Pages 项目的 Custom domains。根域名需先作为 Cloudflare zone 添加并将注册商的 nameservers 改为 Cloudflare 分配的值，然后通过 Pages 完成域名关联和 DNS 设置。待 HTTPS 证书生效后验证访问；按需要配置 www 跳转并更新网站元数据。域名注册和续费是届时新增的成本，本阶段不执行购买或 DNS 变更。

官方文档：
- <https://developers.cloudflare.com/pages/framework-guides/deploy-anything/>
- <https://developers.cloudflare.com/pages/configuration/custom-domains/>
- <https://developers.cloudflare.com/pages/platform/limits/>
