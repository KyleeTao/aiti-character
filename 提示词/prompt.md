# aiti 生图提示词

> 用于复现 aiti 的形象。中英双语，负面词通用。
> 实测：2026-10-25，ImageGen，1536×1024（三视图）/ 1024×1024（Q版），quality=high。

---

## 一、三视图（角色设定稿）

**中文**

```
日系动画风格，赛璐璐上色，角色三视图设定稿 character sheet：同一角色的正面、侧面、背面三个全身视角并排排列，纯白背景。
角色：银灰色渐层短发的猫娘少女，头顶一对银灰猫耳（耳内是电子青渐变，边缘有细发光描边），头顶一根呆毛；
异色瞳——右眼电子青、左眼琥珀色；表情是有点心虚的讨好的笑。
穿米白色 oversize 卫衣，袖口有灰色条纹，背后印一个灰色光标符号；深灰色短裤，
白色过膝袜（袜口一圈电子青细线），白色板鞋。
脖子上戴黑色颈圈，挂一个电青色发光小铃铛。
身后一条银灰长尾，尾巴末端三厘米是半透明的电子青光。
冷色调，干净线稿，高饱和青色光点，背景纯白，三个视角等高并排，全身入镜。
```

**English**

```
Anime style, cel-shaded, character sheet with three full-body views
(front, side, back) of the same character, arranged side by side on a pure white background.
Silver-grey gradient short-haired cat girl, a pair of silver cat ears with cyan glowing
inner ear and thin luminous rim, one ahoge on top;
heterochromia — right eye electric cyan, left eye amber; slightly guilty, eager-to-please smile.
Wearing an oversized off-white hoodie with grey stripe cuffs and a small grey cursor symbol on the back;
dark grey shorts, white thigh-high socks with a thin cyan line at the top, white sneakers.
Black choker with a small glowing cyan bell.
A long silver-grey tail with the last 3 cm translucent cyan glow.
Cool palette, clean lineart, high-saturation cyan accents, pure white background,
three views at equal height, full body.
```

---

## 二、Q 版立绘

**中文**

```
2.5 头身 chibi 比例，大头小身，日系动画风格，赛璐璐上色，Q版猫娘少女全身立绘，纯白背景。
银灰色渐层短发，头顶一对银灰猫耳（耳内电子青渐变，边缘细发光描边），头顶呆毛；
异色瞳——右眼电子青、左眼琥珀色，表情是开心讨好的笑，嘴巴小小张开。
穿米白色 oversize 卫衣（袖口有灰色条纹），深灰色短裤，白色过膝袜（袜口一圈电子青细线），白色板鞋。
脖子戴黑色颈圈，挂一个电青色发光小铃铛。
身后一条银灰长尾，尾巴末梢是半透明电子青光。
冷色调，高饱和青色光点，背景纯白，角色居中，全身入镜。
```

**English**

```
2.5 head-tall chibi proportions, big head, small body,
anime style, cel-shaded, full-body chibi cat girl, pure white background.
Silver-grey gradient short hair, silver cat ears with cyan glowing inner ear and thin luminous rim,
one ahoge; heterochromia — right eye electric cyan, left eye amber;
happy eager-to-please smile with small open mouth.
Oversized off-white hoodie with grey stripe cuffs, dark grey shorts,
white thigh-high socks with a thin cyan line at the top, white sneakers.
Black choker with a small glowing cyan bell.
Long silver-grey tail with a translucent cyan glowing tip.
Cool palette, high-saturation cyan accents, pure white background, centered, full body.
```

---

## 三、负面词（两个 prompt 通用）

```
extra fingers, fused fingers, missing fingers, extra limbs, deformed hands,
distorted face, warped ears, melting face, bad anatomy,
blurry, low quality, jpeg artifacts, watermark, text, logo, busy background
```

> 注意：**不要**把 `asymmetric eyes` 放进负面词——aiti 的异色瞳是设定，放了反而会破坏。

---

## 四、参数建议

| 参数 | 三视图 | Q 版 |
|---|---|---|
| 尺寸 | 1536×1024 | 1024×1024 |
| quality | high | high |
| background | opaque（白底，便于抠图） | opaque |
| 负面上 | 见上 | 见上 |

生成后用 `imgtool.py matte --thresh 42 --feather 2` 抠成透明 PNG。

---

## 五、其他视角 / 表情（待补）

需要时按下列思路扩展，保持同一组风格词：

- **侧面**：「silver cat girl, side view, walking pose, tail curved forward」
- **背面**：「back view, oversized hoodie with grey cursor symbol on the back」
- **表情：懵**：「blank stare, ears slightly drooping, small mouth open」
- **表情：炸毛**：「startled, tail puffed up, ears flat, cyan tip glowing brightly」
- **表情：心虚**：「awkward smile, eyes looking away, one ear tilted down」
