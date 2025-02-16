---
permalink: /pages.html
---



# 如何使用Github Pages

【2025-02-15】

链接：

* 0hujun.github.com
* [Quickstart for GitHub Pages - GitHub Docs](https://docs.github.com/en/pages/quickstart)
* [欢迎 - Jekyll • 简单静态博客网站生成器](https://jekyllcn.com/docs/home/)

## 教程

### 1 关于Github Pages

通过将github仓库中的静态html文件放在github服务端并提供URL访问。

官方提供markdown输入转html的Jekeyll工具，可一键部署转换。

#### 关于发布

直接使用actions workflow发布，如果使用Jekeyll，github会自动发布。

### 2 使用模板



### 3 使用Workflow

#### Action

[Checkout · Actions · GitHub Marketplace](https://github.com/marketplace/actions/checkout)

[Build Jekyll for GitHub Pages · Actions · GitHub Marketplace](https://github.com/marketplace/actions/build-jekyll-for-github-pages)

一个例子

```yaml
name: Build Jekyll site
on:
 push:
   branches: ["main"]
permissions:
  contents: read
  pages: write
  id-token: write
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      - name: Setup Pages
        uses: actions/configure-pages@v5
      - name: Build
        uses: actions/jekyll-build-pages@v1
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
  deploy:
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
```

## 注意事项

### 1 未解析转换文件

[jekyll not generating index.html - Stack Overflow](https://stackoverflow.com/questions/26314435/jekyll-not-generating-index-html)

在html中加入了liquid语法，但是Jekyll未解析。需要在html前加入yaml format格式。

