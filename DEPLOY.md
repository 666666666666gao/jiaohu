# 部署步骤指南

## 方式一：GitHub Pages（推荐，免费）

### 步骤 1：在 GitHub 创建新仓库

1. 访问 https://github.com/new
2. 输入仓库名称（例如：`3d-particle-system`）
3. **不要**勾选 "Initialize this repository with a README"
4. 点击 "Create repository"

### 步骤 2：推送代码到 GitHub

在终端中运行以下命令（将 `你的用户名` 和 `仓库名` 替换为实际值）：

```bash
# 添加远程仓库
git remote add origin https://github.com/你的用户名/仓库名.git

# 重命名分支为 main（如果GitHub要求）
git branch -M main

# 推送代码
git push -u origin main
```

**注意**：如果这是第一次推送，GitHub 可能会要求你输入用户名和密码（或使用 Personal Access Token）

### 步骤 3：启用 GitHub Pages

1. 在 GitHub 仓库页面，点击右上角的 **Settings**（设置）
2. 在左侧菜单中找到 **Pages**（页面）
3. 在 "Source" 下选择：
   - Branch: `main`
   - Folder: `/ (root)`
4. 点击 **Save**（保存）
5. 等待几分钟，GitHub 会生成你的网站地址：
   - 格式：`https://你的用户名.github.io/仓库名/`

### 步骤 4：访问你的网站

部署完成后，访问 GitHub 提供的地址即可！

---

## 方式二：Netlify（最简单，拖拽即可）

### 步骤 1：访问 Netlify

访问 https://www.netlify.com/ 并登录（可以用 GitHub 账号登录）

### 步骤 2：部署

1. 在 Netlify 控制台，找到 **"Sites"** 页面
2. 将包含 `index.html` 的文件夹拖拽到部署区域
3. 等待部署完成
4. Netlify 会自动给你一个免费域名（例如：`random-name-123.netlify.app`）

### 步骤 3：自定义域名（可选）

在 Netlify 设置中可以添加自定义域名

---

## 方式三：Vercel（适合开发者）

### 步骤 1：访问 Vercel

访问 https://vercel.com/ 并登录（可以用 GitHub 账号登录）

### 步骤 2：导入项目

1. 点击 **"Add New..."** → **"Project"**
2. 选择从 GitHub 导入，或直接上传文件夹
3. 点击 **"Deploy"**
4. 等待部署完成

---

## 方式四：本地测试

如果你想先在本地测试，可以运行：

```bash
# Python 3
python -m http.server 8000

# 或使用 Node.js
npx http-server -p 8000
```

然后访问：http://localhost:8000

---

## 常见问题

### Q: GitHub Pages 显示 404？
A: 确保仓库是公开的（Public），或者升级到 GitHub Pro 才能使用私有仓库的 Pages

### Q: 网站加载很慢？
A: 首次加载需要下载 Three.js 等库，稍等片刻即可

### Q: 摄像头功能不工作？
A: 确保使用 HTTPS 访问（GitHub Pages、Netlify、Vercel 都默认使用 HTTPS）

---

## 推荐

- **初学者**：使用 Netlify，拖拽即可
- **有 GitHub 账号**：使用 GitHub Pages，完全免费
- **需要自定义域名**：使用 Netlify 或 Vercel

