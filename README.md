# tchao8820.github.io

GitHub Pages **用户站仓库**。目前只放一份 `robots.txt`。

## 为什么需要这个仓库

爬虫只读取**主机根目录**的 `robots.txt`。Google 官方文档明确说明：子目录中的
`robots.txt`（如 `https://example.com/folder/robots.txt`）不是有效文件，抓取工具不会检查。

项目仓库 [`ctbu-kexie-website`](https://github.com/tchao8820/ctbu-kexie-website) 位于
子路径 `/ctbu-kexie-website/`，它自己生成的 `robots.txt` 虽然能被下载，但爬虫不会
读取其中的规则。放在本仓库后，`https://tchao8820.github.io/robots.txt` 生效，
对该用户名下**所有 Pages 项目页**统一生效。

## 文件

| 文件 | 作用 |
|---|---|
| `robots.txt` | 爬虫规则 + sitemap 声明，覆盖主机根 |
| `.nojekyll` | 阻止 GitHub Pages 走 Jekyll 构建，保证原样发布 |

## 维护

本文件为**手工维护**，非脚本生成。新增 Pages 项目后，请同步更新：

1. `Sitemap:` 行（每个需要收录的站点一行）
2. 项目专属的 `Disallow` 规则

注意：**不要**屏蔽 `/assets/`—— 那是站点真实使用的图片目录，屏蔽后
`og:image` 与正文配图将无法被抓取，影响图片搜索收录。

## 关联

- 官网仓库：<https://github.com/tchao8820/ctbu-kexie-website>
- 线上地址：<https://tchao8820.github.io/ctbu-kexie-website/>