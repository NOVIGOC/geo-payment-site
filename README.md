# GEO 推广预付费网站

这是一个纯静态网站项目，可以直接部署到任何支持静态文件托管的平台。

## 项目文件

- `index.html`：网页主文件
- `address-map.png`：地址地图图片
- `review-avatars.png`：评价头像图片

## 推荐部署方式

### 方式 1：Netlify

最简单，适合现在直接发给别人看。

1. 打开 [Netlify](https://app.netlify.com/drop)
2. 把整个项目文件夹拖进去
3. 等待生成公开链接
4. 把 `*.netlify.app` 链接发给别人

这个项目已经包含 `netlify.toml`，Netlify 会直接把当前目录当成发布目录。

### 方式 2：GitHub Pages

适合后续继续维护和更新。

1. 新建一个 GitHub 仓库
2. 把当前目录里的所有文件上传到仓库根目录
3. 确保默认分支是 `main`
4. 这个项目已经内置 GitHub Pages 工作流：
   `.github/workflows/pages.yml`
5. 在 GitHub 仓库里打开 `Settings`
6. 找到 `Pages`
7. 在 `Build and deployment` 中把 `Source` 选择成 `GitHub Actions`
8. 等待 Actions 跑完，GitHub 就会生成公开链接

项目里已经加入：

- `.nojekyll`
- `.github/workflows/pages.yml`

以后只要往 `main` 分支推送更新，GitHub Pages 就会自动重新发布。

## 本地预览

直接双击 `index.html` 即可。

如果想用本地服务器方式预览，可以在当前目录运行：

```bash
python3 -m http.server 8080
```

然后打开：

`http://localhost:8080`

## 更新网站

以后只要改这几个文件并重新上传，就可以覆盖发布：

- `index.html`
- `address-map.png`
- `review-avatars.png`
