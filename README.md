# viz-studio · 视觉工作室

一个以「参考图 → 像素实测 → 风格分册 → HTML/CSS 出图」为方法论的海报级视觉技能（Agent Skill）。核心方法是用 HTML/CSS 写图（固定画布，不调 AI 生图）——文字永远锐利、配色可控、改稿定点改不重做。

## 能做什么

11 类物料：小红书封面 / 公众号封面 / 讲座·年会·活动主视觉 KV / 电子邀请函 / 宣传海报 / 数据长图 / 名片 / 三折页 / 易拉宝 / 道旗 / PPT。

四种输入模式：

- **A 文案直出**——给文字，五问追问定稿后按分册排版出图
- **B 图片复刻**——给参考图，网格测量、取色、逐字复刻
- **C 换风格改配色**——同版式只动 `:root` tokens 与字体栈
- **D 自由模式**——只守护栏与 tokens、不套布局原型的原创构图（`references/freestyle.md`）

## 13 个风格族（13/13 定稿）

| 风格族 | 一句话特征 |
|---|---|
| tech-beam-dark 暗夜光束 | 暗底 + 放射光效 + 居中大字 |
| organic-sweep 有机曲面 | 黄绿大渐变曲面 + 白色飘带 + 巨字 |
| editorial-swath 材质编辑 | 深绿底 + 中央材质摄影卡 + 衬线 |
| newchinese 新中式 | 纸纹底 + 宋/明体大字 + 直排 |
| zen-collage 日系拼贴 | 白底黑宋阶梯标题 + 真实照片拼贴 + 红点睛 |
| tech-air-longform 浅色科技长图 | 浅蓝白渐变 + 3D 飘带 + 圆角玻璃卡 |
| ivory-gold 象牙金 | 米白底 + 金主色 + 鎏金插画 + 衬线大写字标 |
| veil-glow 光影纱幕 | 柔焦光影渐变底 + 衬线/书法大字 |
| silk-flare 绸缎鎏金 | 暗红黑底 + 绸缎光影 + 金白衬线，重奢华 |
| data-graphic 数据图形 | 大数字 + 模块网格 |
| editorial-block 色块编辑 | 大色块 + 人像摄影 + 杂志层级 |
| quote-pop 金句海报 | 大底色 + 黑白人像 + 引言 + 胶囊标签 |
| split-portrait 半版人像 | 暗底噪纹 + 半版人像渐隐 + 几何刀口 + 巨型标题 |

## 目录结构

```
viz-studio/
├── SKILL.md            # agent 入口路由器（流水线 Step 0–6 / 格式路由表 / 铁律十条）
├── ASSETS.md           # 素材确权清单（商用授权状态）
├── README.md           # 本文件
├── references/
│   ├── guardrails.md   # 唯一必读护栏（含 §9 自检清单）
│   ├── freestyle.md    # 自由模式协议（novelty 判定 + 必经五步）
│   └── styles/         # 13 份九段风格分册 + 各族案例图库 case-*.png
├── fonts/              # 内置 10 款字体（自包含，授权表见 fonts/FONTS.md）
├── trials/             # 各族蒸馏期试做复刻
└── tests/              # 真单验收记录
```

## 安装（Claude Code / 兼容 agent 环境）

1. 解压后将文件夹命名为 `viz-studio`（须与 SKILL.md frontmatter `name: viz-studio` 一致）
2. 复制到 `~/.claude/skills/viz-studio/`
3. 新开会话，说「做一张小红书封面 / 出一张邀请函」即触发

## 字体与素材授权

- 内置 10 款字体（思源黑/宋、MiSans、LXGW 文楷、漓雨手书、EB Garamond、Bodoni Moda、Roboto Flex、Rozha One），授权明细见 `fonts/FONTS.md`
- 素材商用确权状态见 `ASSETS.md`（2026-10-13 确权）
- 已知引擎注意：`@font-face` 的 `font-weight` 描述符不要写端点字重（如 `400 700` 时请求 400 会静默回退系统字体），统一写 `300 800` 这类内区间

## 验证记录（tests/）

- 真单 #1：ivory-gold 电子邀请函 1080×2340，全新文案冷启动（`realorder-01-invitation/`）
- 真单 #2：讲座主视觉 KV 1920×1080（`realorder-02-lecture-kv/`）
- 真单 #3：年会邀请函 veil-glow A 1080×2340（`realorder-03-annual-gala/`）
- 自由模式验证：周年刻度盘邀请函 1080×1440（`freestyle-01-gala/`）

## 血统

流程与护栏蒸馏自 artboard（GreenChennai）；PPT 基座复用归藏 guizang-ppt-skill；13 份风格分册均由用户提供的真实模板/参考图经「做 → 批 → 改」两三轮蒸馏收敛而成。
