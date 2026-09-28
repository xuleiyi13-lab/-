# Deconstructed Duotone Poster

[English README](README_EN.md)

这是一个用于 ChatGPT / Codex 的图片风格化 Skill。它会先识别图片里的主体，再把主体拆成一组平面图形，做成双色、柔光、纸纹和胶片颗粒感的编辑海报。

## 效果示例


<p align="center">
  <img src="examples/food-before-after.webp" alt="食物照片与六宫格海报对比" width="31%">
  <img src="examples/ducks-before-after.webp" alt="水面双鸭照片与六宫格海报对比" width="31%">
  <img src="examples/lighthouse-before-after.webp" alt="灯塔照片与六宫格海报对比" width="31%">
</p>

<p align="center">
  <img src="examples/purple-canopy.webp" alt="紫色树冠九宫格海报" width="31%">
  <img src="examples/tables-after-dusk.webp" alt="砖红色夜晚餐桌九宫格海报" width="31%">
  <img src="examples/bright-bursts.webp" alt="橙色烟花九宫格海报" width="31%">
</p>

## 它能做什么

- 把照片改造成 3:4 竖版九宫格海报。
- 把竖图改造成 3:4 竖向四联画海报。
- 把横版照片改造成 4:3 横版六宫格海报。
- 把横图改造成 4:3 横向四联画海报。
- 不提供照片时，也可以直接根据文字主题生成。
- 可以在原图基础上再加入一个指定主体。
- 米白纸底固定，另一种主题色由你指定。
- 自动加入两行小字和与画面主体有关的极简图标。

每个格子不会重复画同一张照片。Skill 会挑选轮廓、动作、材质和局部特征，再用不同的平面图形重新表达。最终画面更像印刷海报，不像照片滤镜。

## 四种版式

| 版式 | 画幅 | 内容 | 适合 |
| --- | --- | --- | --- |
| 九宫格 | 3:4 竖版 | 3×3 方格 | 竖图、方图、文字主题 |
| 竖向四联画 | 3:4 竖版 | 1×4 方格 | 需要更简洁的竖图 |
| 六宫格 | 4:3 横版 | 3×2 方格 | 横图、宽场景 |
| 横向四联画 | 4:3 横版 | 4×1 方格 | 需要更简洁的横图 |

四种版式都保留较多留白。顶部与左右两侧的距离相同，每个格子都是标准正方形。四联画适合主体很明确、希望画面更克制的图片。

## 画面特点

- 大块平面图形，不照搬原照片。
- 细节适中，不使用彩铅、排线或写实质感。
- 浅米白纸底加一种主题色。
- 图形边缘有轻微的手工印刷感。
- 柔光与光晕比较明显，但图形主体仍然清楚。
- 带有自然纸纹和细颗粒。
- 底部只有两行小字和一至五个主体图标。

## 安装

下载或克隆这个仓库，把完整的 `deconstructed-duotone-poster` 文件夹安装为自定义 Skill。不要只复制 `SKILL.md`，因为版式参考图和其他规则文件也需要一起保留。

本地 Codex 可以使用：

```bash
git clone https://github.com/Lixorn/deconstructed-duotone-poster.git
mkdir -p ~/.codex/skills
cp -R deconstructed-duotone-poster/deconstructed-duotone-poster ~/.codex/skills/deconstructed-duotone-poster
```

## 使用方法

使用时只需要提供图片和主题色：

```text
用 $deconstructed-duotone-poster 风格化这张照片，主题色使用浅蓝色。
```

指定横版六宫格：

```text
用 $deconstructed-duotone-poster 把这张横图做成 4:3 六宫格，主题色使用绿色。

用 $deconstructed-duotone-poster 把这张横图做成 4:3 横向四联画，主题色使用海蓝色。

用 $deconstructed-duotone-poster 把这张竖图做成 3:4 竖向四联画，主题色使用砖红色。
```

不提供图片，直接写主题：

```text
用 $deconstructed-duotone-poster 做一张关于公路、沙滩和大海的砖红色海报。
```

在原图中加入新主体：

```text
用 $deconstructed-duotone-poster 处理这张海岸照片，再加入一辆敞篷车，主题色使用钴蓝色。
```

一次处理多张图片时，可以分别指定颜色：

```text
用 $deconstructed-duotone-poster 处理这三张照片，分别使用青色、红色和紫色。
```

## 三种主要模式

| 模式 | 你需要提供什么 | 结果 |
| --- | --- | --- |
| 图片模式 | 一张或多张图片 | 从每张图中提取主体并重新设计 |
| 文字主题模式 | 一段简短主题 | 根据文字直接创作画面 |
| 图片加主体模式 | 原图和要加入的主体 | 保留原图主题，同时加入新主体 |

如果只想查看生成提示，可以要求“只给 Prompt”。如果只想分析风格，可以要求“只分析，不生成”。

## 颜色

主题色可以直接写颜色名称，例如浅蓝色、砖红色、森林绿或紫色，也可以提供十六进制色值。默认纸底固定为较浅的米白色 `#F7F1E3`。

Skill 默认使用米白色加一种主题色。如果你明确要求多色，也可以根据画面主体使用少量受控颜色，例如为不同食物分别保留对应颜色。

## 文件结构

```text
.
├── README.md
├── README_EN.md
├── LICENSE
├── examples/
└── deconstructed-duotone-poster/
    ├── SKILL.md
    ├── agents/
    ├── assets/
    └── references/
```

## 许可

使用 [MIT License](LICENSE)。
