# Hello GPU 图解教材(大白话可视化版)

> 原著:[datawhalechina/hello-gpu](https://github.com/datawhalechina/hello-gpu)(dev 分支,全 20 章)
> 本仓库:把原著重写成**看得懂的白话 + 画出来的原理 + 敢记录的负结果**,纯静态页面,零依赖,GitHub Pages 直接托管。

**📖 在线阅读：** [https://huangtietuo.github.io/hello-gpu-illustrated/](https://huangtietuo.github.io/hello-gpu-illustrated/)(浏览器直接打开,无需安装,桌面/移动端自适应)

## ✨ 这是什么

- **20 章全覆盖**,组织为 5 个部分页 + 1 个首页地图 + 1 个交互加强页:

| 文件 | 内容 |
|---|---|
| `index.html` | 首页:全书地图、5 大部分导航、20 章一句话索引、学习路线 |
| `part0.html` | 入门篇(第 0-4 章):GPU 心智模型、环境三道门、第一个 kernel |
| `part1.html` | Profiling 篇(第 5-7 章):可信计时、rocprof、Roofline(含 SVG 示意图) |
| `part2.html` | 算子篇(第 8-13 章):逐元素/归约/Softmax/GEMM/融合/RMSNorm |
| `part3.html` | Agent 篇(第 14-17 章):Agent 闭环、工具封装、10 轮实战账本 |
| `part4.html` | 实战篇(第 18-19 章):YOLO 部署、LLM decode 实测 |
| `chapter8-elementwise.html` | 第 8 章交互加强版:依赖动画、工号计算器、合并访存动画、Triton mask 演示、小测验 |

- 所有数据(耗时、带宽、加速比)引自原文实测(RX 9070 XT / ROCm 7.13 等基线平台),未实测的章节如实标注 Alpha。
- 本站是**学习辅助材料**,代码与完整推导以[原文](https://github.com/datawhalechina/hello-gpu)为准。

## 🚀 部署到 GitHub Pages(3 步)

1. **创建仓库**:在 GitHub 上新建仓库,推荐名称 **`hello-gpu-illustrated`**(备选:`hello-gpu-viz`、`gpu-baihua`)。不要勾选自动生成 README(本目录已有)。

2. **推送本目录全部文件**:

   ```bash
   cd 本目录
   git init
   git add .
   git commit -m "Hello GPU 白话图解教材(20章)"
   git branch -M main
   git remote add origin https://github.com/<你的用户名>/hello-gpu-illustrated.git
   git push -u origin main
   ```

3. **开启 Pages**:仓库 → Settings → Pages → Build and deployment → Source 选 **Deploy from a branch** → Branch 选 **main** / **/(root)** → Save。

一两分钟后访问 `https://<你的用户名>.github.io/hello-gpu-illustrated/` 即可。

> 想绑定自定义域名或用 Actions 部署也可以,纯静态站无需任何构建步骤。

## 🧭 推荐学习路线

- **零基础**:入门 → 量准 → 算子 → Agent → 实战(顺序读,约 2-3 周,每天 2-3 小时)
- **CUDA 老手**:直接算子篇 + Agent 篇,计时问题回第 5 章
- **只懂原理**:第 7 章(Roofline)+ 算子篇

## 📄 版权与致谢

内容重制自 datawhalechina 的开源教材 **hello-gpu**,版权归原作者所有;本仓库仅作学习交流用途。
