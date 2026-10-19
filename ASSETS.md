# ASSETS.md · 素材确权清单

> 用途：登记 skill 内所有非生成素材（照片/3D 物件/抠图）的来源与授权状态。
> 规则：**试做与复刻**（skill 内部校准、用户过会）可直接使用任何素材；**商用交付**前必须满足「✅ 可商用」或完成「⚠️ 待确权」的确认。字体均为可商用开源（思源黑体/宋体、Roboto Flex、MiSans），不在此列。
>
> **确权裁定（2026-10-13）：用户确认「素材目前没什么问题，可以商用」——清单内全部现行素材商用授权落定。**⚠️ 状态此后仅保留给**新增**的未登记素材。
>
> 状态图例：✅ 授权明确可商用 · ⚠️ 待确权（商用前需用户确认）· 🔁 有合规替换件

## 一、花瓣网系列（用户提供）✅ 已确权（2026-10-13 用户整体确认）

均来自花瓣网采集（huaban.com，图床转载，原始出处/作者不明）。花瓣网本身不授版权；**2026-10-13 用户整体确权「素材目前没什么问题，可以商用」，四件警告解除。**后续若新增花瓣源素材，仍需单独确权。

| 文件 | 尺寸 | 登记来源 | 现行用途 | 替换方案 |
|---|---|---|---|---|
| `trials/ivory-gold/assets/golden-horse-gallop.png` | 631×473 RGBA | 花瓣 huaban-7031607399 | **ivory-gold A 现行主视觉**（v6 鎏金水墨奔马，2026-10-10 过会） | `white-horse-cutout.png`（同构图语感） |
| `trials/ivory-gold/assets/golden-horse-ink.png` | 400×474 RGBA | 花瓣（同批采集） | A v5 遗留（水墨立马，已被 v6 奔马取代） | 同上 |
| `trials/ivory-gold/assets/white-horse-front.png` | 369×536 RGBA | 花瓣（同批采集） | A v2–v4 遗留（白马正面） | 同上 |
| `trials/tech-air-longform/assets/huaban-glass-ribbon.png` | 420×282 RGBA | 花瓣 huaban-6305481218 | **tech-air-longform 现行 3D 玻璃飘带** | **SVG 兜底配方**（tech-air-longform.md §7.1，交付时声明「SVG 兜底、非 3D 素材」） |

## 二、合规素材 ✅

| 文件 | 尺寸 | 来源与授权 | 现行用途 | 署名要求 |
|---|---|---|---|---|
| `trials/zen-collage/assets/mist-layers.jpg` | 1920×1280 | Wikimedia Commons「Breath of the Mountains」© Nuiza11，**CC BY-SA 4.0** | zen-collage 试做（裁切+调色，许可允许） | **商用必须署名**（作者+许可+链接） |
| `trials/ivory-gold/assets/white-horse-gold-field.jpg` | 1920×1247 | Wikimedia Commons「Silver shadow」© Bernard Spragg. NZ，**Public Domain** | ivory-gold A 候选 | 无 |
| `trials/ivory-gold/assets/white-horse-cutout.png` | 1149×797 RGBA | Unsplash 原图 + 本地 GrabCut 抠图（Unsplash License 可商用） | ivory-gold A 合规替换件（金马替换候选） | 无强制（Unsplash 许可） |

## 三、人像素材 ✅ 已确权（2026-10-13 用户整体确认；来源未登记）

| 文件 | 尺寸 | 状态 |
|---|---|---|
| `trials/editorial-block/assets/speaker-portrait.jpg` | 1600×2327 | 来源未登记（无出处注释；分册规则：暗底人像可用 Unsplash 直链，网络不可达时本地素材+声明）。与 quote-pop 副本**字节相同**（md5 4b9cc5a2），改一处即同步两处 |
| `trials/quote-pop/assets/speaker-portrait.jpg` | 1600×2327 | 同上（副本） |

确权记录（2026-10-13）：用户整体确认可商用，警告解除。来源登记留待需对外披露出处时再处理（届时按 editorial-block.md 规则换 Unsplash 直链新图或换用户自有授权件）。

## 四、纯生成素材（无需确权，备查）

A 奔马 Photoshop 合成稿（`golden-horse-gallop.png` 的加工说明）、全部 SVG 几何图形（B 缎带漩涡扇面、quote-pop 字形嵌像框架、tech-air SVG 兜底飘带）、全部渐变/噪点底纹均为代码生成，无第三方版权。

## 五、待办

- [x] 用户确认花瓣网四件素材的商用授权（2026-10-13 整体确权 ✅）
- [x] speaker-portrait.jpg 商用确权（2026-10-13 用户整体确认覆盖；来源登记留待披露需要）
- [ ] zen-collage 商用交付时附署名行：「照片: Breath of the Mountains © Nuiza11 (CC BY-SA 4.0)」（交付时动作，非阻塞）
