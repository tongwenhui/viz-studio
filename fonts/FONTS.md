# viz-studio-skill 内置字体库

技能自包含字体库（2026-10-10 从项目 `artboard/fonts/` 拷贝入库，文件逐字节一致，目录结构与其一致）。
所有风格分册与试做 HTML 的 `@font-face` 一律使用**技能内相对路径**，禁止引用技能外部路径、禁止 CDN。

## 挂载约定

- 试做图（`trials/<族>/replica-*.html`）→ `../../fonts/<家族>/<文件名>`
- 新项目产线 HTML：把所需字体拷入项目（如 `<项目>/fonts/`）后引用 `fonts/<家族>/<文件名>`，渲染完可删。
- 导出引擎 @font-face 端点 bug 仍然有效：区间描述符写 `300 800`（EB）/`200 900`（Noto），CSS 请求字重不得落在区间端点上（详见 ivory-gold 分册 §3）。

## 字体清单

| 技能内路径 | 用途 | 授权 | 备注 |
|---|---|---|---|
| fonts/source-han-sans/NotoSansSC-VF.ttf | 无衬线中文主力（data-graphic/organic-sweep/editorial-block/tech-air-longform/split-portrait） | SIL OFL 1.1 | VF，wght 100–900 |
| fonts/source-han-serif/NotoSerifSC-VF.ttf | 宋体/衬线中文主力（veil-glow/newchinese/zen-collage/silk-flare/ivory-gold 等） | SIL OFL 1.1 | VF，描述符须 `200 900` |
| fonts/english-eb-garamond/EBGaramond-Regular.ttf | Latin 衬线（多族通用） | SIL OFL 1.1 | 描述符须 `300 800`；数字禁用（oldstyle），数字走系统 Times New Roman |
| fonts/english-eb-garamond/EBGaramond-Italic.ttf | 意大利体点缀（silk-flare） | SIL OFL 1.1 | |
| fonts/english-bodoni-moda/BodoniModa-VF.ttf | Didone 巨字（ivory-gold INVITATION） | SIL OFL 1.1 | VF，`'opsz' 96,'wght' 400` 出发丝级高反差 |
| fonts/liyu-shoushu/LiyuShoushu.ttf | 书法手写（veil-glow/newchinese/editorial-block） | 免费商用（漓雨手书） | 单字重 |
| fonts/lxgw-wenkai/LXGWWenKai-Regular.ttf | 楷体（organic-sweep/veil-glow 兜底） | SIL OFL 1.1 | |
| fonts/misans/MiSans-Regular.ttf | 备选无衬线（tech-beam-dark） | 小米 MiSans 免费商用 | 仅 Regular |
| fonts/english-roboto-flex/RobotoFlex-VF.ttf | 几何无衬线 Latin（tech-beam-dark/split-portrait） | SIL OFL 1.1 | VF，wght 100–1000，单层 g |
| fonts/english-rozha-one/RozhaOne-Regular.otf | 备用 Didone（silk-flare 备选） | SIL OFL 1.1 | 过重，ivory-gold 已否决 |

授权详情见项目参考库 `artboard/fonts/<家族>/INTRO.md`。
