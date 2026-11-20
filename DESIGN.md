# DESIGN

## Direction

一页一张现场照片，右侧是台词与答案，其余全部删掉。字号优先：投影和电脑上都一眼看清。

## Tokens

```
--paper    oklch(0.964 0.011 84)   暖纸白
--ink      oklch(0.235 0.012 65)
--ink-2    oklch(0.455 0.012 65)
--rule     oklch(0.868 0.010 78)
--offer    oklch(0.53 0.17 33)     朱：要约人
--accept   oklch(0.42 0.085 252)   靛：受要约人
```

## Type

- 台词：楷体，clamp(28px, 3.1vw, 50px)（第三场长台词降到 2.7vw）
- 角色名与答案：同一字号，宋体标签 + 楷体答案，clamp(28px, 3vw, 46px)
- 页脚只有场次编号和「下一场」，14px

## Layout

左图右文，两栏各自垂直居中。图片保持 1800×935，右侧宽度下限 400px，保证「受要约人：手机店老板」一行放得下。

## Motion

场景淡出淡入；答案上浮 12px 浮现，角色色细线从左画开。尊重 prefers-reduced-motion。

## Constraints

- 单文件 HTML + 本地 WebP，双击即可打开
- 电脑/投影优先；≤880px 自动单列
