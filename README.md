# PixelBead 拼豆图纸工坊

AI 一键将图片转为 MARD / Hama 色板拼豆图纸 · 国内 2.6mm 迷你豆 + Hama 5mm 标准豆 · 全前端 · 移动端友好

🌐 **在线体验**：https://sageautoman.github.io/pixel-bead-generator/

## 功能

- 📤 上传图片自动生成像素图纸（写实 / Q版双方案）
- 🎨 多品牌色板：MARD 291 色 / Hama Midi 53 色，一键切换 + Lab 重映射
- ✨ 5 种豆子样式预览（普通 / 空心 / 毛巾烫 / 细闪 / 粗闪）
- 🖼️ 一键描边（黑 / 白 / 自定义）
- ✂️ 自动摘除背景（边界连通约束，主体内部相似色保留）
- 📐 支持 16² / 29² / 50² / 58² 多尺寸
- 📊 行列坐标 + 每格色卡序号编号
- 🖨️ 打印 / 导出 PDF（A4 自动适配 + 紧凑 3 列用料对照表）
- 📱 移动端底部工具栏 + 抽屉式色板 + 双指缩放

## 部署

零依赖，单 HTML 文件。直接打开 `index.html` 即可，或托管到任意静态服务器：

- GitHub Pages（当前在用）
- Vercel / Netlify / Cloudflare Pages
- 任意 nginx / Apache

## 技术栈

- 纯 HTML + CSS + Canvas，无构建步骤
- 像素化算法：USM 锐化 + Sobel 边缘 + 边缘感知降采样
- 抠图：Lab 空间聚类 + 边界 flood-fill
- 色板切换：CIE Lab 距离最近邻重匹配
- 豆子样式：mulberry32 PRNG + 全局烫纸 overlay

## License

MIT
