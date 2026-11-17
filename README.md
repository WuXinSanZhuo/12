# 

这是 https://fabric-tear.vercel.app/ 的静态镜像，用于在国内网络下直接访问。
所有资源（HTML / JS / CSS / 模型 / 贴图 / 音效）均为同源本地文件，不依赖任何 CDN。

## 部署到 GitHub Pages（全程网页操作，不用装 git）

1. 打开 https://github.com/new
   - Repository name 填 `fabric-tear`（或任意名字）
   - 选 **Public**（免费账号只有公开仓库能开 Pages）
   - 点 **Create repository**

2. 进入仓库页面，点 **uploading an existing file**（或 Add file → Upload files）
   - 把这个文件夹里的 **全部内容** 拖进去：
     `index.html`、`assets/`、`releases/`、`README.md`
   - 注意：要拖 **文件夹里的东西**，不要拖外层文件夹本身，否则会多一层目录
   - 点 **Commit changes**

3. 仓库页面 → **Settings** → 左侧 **Pages**
   - Source 选 **Deploy from a branch**
   - Branch 选 **main**，目录选 **/ (root)**
   - 点 **Save**

4. 等 1–2 分钟，刷新 Settings → Pages，顶部会出现网址：
   `https://<你的用户名>.github.io/fabric-tear/`

## 说明

- 首页就是 `index.html`，无需构建、无需 Node。
- 整个站点约 12 MB，其中模型文件 6.9 MB、贴图 3 MB。
- `.nojekyll` 用于关闭 Jekyll 处理，避免以下划线开头的文件被忽略。
- `*.github.io` 在国内一般可直连（偶尔慢），比 `*.vercel.app` 稳定得多。
  如果哪天也不通，可把同一份文件再传到 EdgeOne Pages（`*.edgeone.app` 国内可直连）。

## 自定义域名（可选）

GitHub Pages 支持绑定自己的域名：
Settings → Pages → Custom domain 填入域名 → 在你的 DNS 里加一条 CNAME 指向 `<用户名>.github.io` → 勾选 Enforce HTTPS。
免费域名（eu.org、us.kg 等）审核和稳定性都一般，不折腾的话直接用 `github.io` 子域即可。

## 版权

页面与模型素材版权归原作者所有，本仓库仅作个人访问用途，请勿用于商业分发。
