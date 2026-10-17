# 上线到 GitHub Pages（3 分钟）

这个文件夹里就是完整网站，不需要任何后端、不需要构建：

- `index.html` —— 网站本体
- `seed.js` —— 9 件内置商品（图片已抠好、内嵌在里面）
- `assets/zpix.ttf` —— 像素字体
- `.nojekyll` —— 让 GitHub Pages 原样发布（不要删）

## 步骤

1. 打开 github.com → 新建一个仓库（New repository），名字随意，比如 `closet-lab`，选 **Public**，创建。
2. 进入仓库 → **Add file → Upload files** → 把**这个文件夹里的所有东西**（`index.html`、`seed.js`、`assets` 文件夹、`.nojekyll`、这个说明）一起拖进去 → **Commit changes**。
   ⚠️ 注意：要保留 `assets` 这个**文件夹**的结构，不要只把里面的字体文件单独拖进去。
3. 仓库 → **Settings → Pages** → Source 选 **Deploy from a branch** → Branch 选 **main**、目录选 **/ (root)** → Save。
4. 等 1–2 分钟，刷新页面，顶部会出现网址，形如：
   `https://你的用户名.github.io/closet-lab/`
5. 打开它 —— **应该直接看到挂满 9 件衣服的衣架**。
   商家后台：在网址后面加 `?mode=admin`。

## 如果打开还是空衣架

99% 是 `seed.js` 没上传成功（没跟 `index.html` 在同一层）。
检查：浏览器打开 `https://你的网址/seed.js`，能看到一大段 `window.SEED_ITEMS = [...]` 就说明没问题。
