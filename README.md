# 韩小梵 · COMSOL 仿真笔记

一个简洁的技术展示单页，用来介绍使用 COMSOL Multiphysics 完成的饱和电抗器三维建模与磁场仿真。无 JavaScript、无第三方依赖。

## 预览

直接双击 `index.html`，或在项目目录启动本地服务器：

```bash
python -m http.server 8000
```

然后访问 `http://localhost:8000`。

## 页面内容

1. 三维几何模型
2. 铁芯与绕组结构
3. 线圈与激励设置
4. 50 Hz 下的磁通密度分布

首页同时列出了研究对象、仿真平台、激励频率和关注结果。

## 文件结构

```text
个人网页blog/
├── index.html                    # 页面文字内容
├── styles.css                    # 样式与响应式布局
├── favicon.svg                   # 网站图标
├── 电抗器3D模型.png               # 原始图片（保留）
├── 饱和电抗器.png                 # 原始图片（保留）
├── 输入.png                       # 原始图片（保留）
├── 铁芯温度.png                   # 原始图片（保留）
├── images/
│   ├── 01-reactor-model.webp     # 三维几何模型
│   ├── 02-reactor-winding.webp   # 铁芯与绕组
│   ├── 03-coil-input.webp        # 线圈与输入
│   └── 04-flux-density.webp      # 磁通密度结果
└── README.md
```

网页使用无损 WebP 副本，原始 PNG 图像未改动。

## 关于图片说明

- `铁芯温度.png` 的画面实际显示的是 50 Hz 下的**磁通密度模分布**（图例单位为 T），因此页面将其描述为磁场结果，并说明其可用于后续铁损和温升分析。
- `输入.png` 的局部信息较少，页面只做了概括性的「线圈与激励设置」描述。如果它对应的是特定的电压、电流或电路输入，请在 `index.html` 中补充准确参数。
- 第 4 部分目前没有展示温度云图。如需强调铁芯温升，可补充一张 COMSOL 温度结果图，并替换 `images/04-flux-density.webp` 或新增一个展示条目。

## 修改内容

- 标题、姓名、介绍和仿真信息：编辑 `index.html`
- 每条图片的标题、说明和标签：修改对应的 `<article class="sim-entry">`
- 配色：修改 `styles.css` 顶部的 CSS 变量（`--paper`、`--ink`、`--accent` 等）

## 发布

这是纯静态页面，可直接部署到 GitHub Pages、Vercel、Netlify 或任意静态托管服务。
