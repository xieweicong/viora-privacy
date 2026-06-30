# Viora 隐私政策 / 支持站点

纯静态站点，给 App Store Connect 提供必填的**隐私政策 URL**、**服务条款 URL** 和**支持 URL**。
无构建步骤、无依赖，直接用 GitHub Pages 托管即可。

## 文件
- `index.html` — 首页
- `privacy.html` — 隐私政策（健康类必填，中英双语）
- `terms.html` — 服务条款（含订阅自动续订说明）
- `support.html` — 支持页（联系邮箱 + FAQ）
- `style.css` — 样式

## 部署到 GitHub Pages
1. 新建一个公开仓库（例如 `viora-site`），把本文件夹内容放到仓库根目录。
2. 仓库 Settings → Pages → Source 选 `Deploy from a branch`，分支选 `main` / 根目录 `/`。
3. 等几分钟，页面地址形如 `https://<用户名>.github.io/<仓库名>/`。

## 上线前务必替换
- 联系邮箱已设为 `xieweicong95@gmail.com`（如需更换全局搜索替换）。
- 部署后把以下 URL 填进 App Store Connect：
  - 隐私政策 URL → `.../privacy.html`
  - 支持 URL → `.../support.html`
  - （可选）服务条款 / EULA → `.../terms.html`
- 把同样的隐私政策 / 支持 URL 一并填到 App 内「设置 › 隐私说明」如有外链。

## 内容依据
隐私政策的数据边界严格对应实际实现：健康原始数据本机不上云、对话/账号/偏好/订阅/用量上云、
AI 经 Supabase 代理调用 OpenRouter（备用 Gemini）。如后端数据流变化，需同步更新 `privacy.html`。
