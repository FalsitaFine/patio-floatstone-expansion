# 素材来源与授权 · Credits

## 音效（`web/sfx/`）

全部来自 **Kenney.nl** 的免费素材包，授权为 **CC0 1.0 Universal（公共领域奉献）**。
CC0 不要求署名，这里仍然列出来源以便核查。

- 来源站点：https://kenney.nl/assets
- 授权文本：https://creativecommons.org/publicdomain/zero/1.0/
- 使用的素材包：
  - **Interface Sounds** — https://kenney.nl/assets/interface-sounds
  - **Impact Sounds** — https://kenney.nl/assets/impact-sounds
  - **RPG Audio** — https://kenney.nl/assets/rpg-audio
  - **Music Jingles** — https://kenney.nl/assets/music-jingles

处理：从原始包里挑出下面这些短音，用 ffmpeg 转成单声道 44.1 kHz 的 `.ogg`（Vorbis）和 `.mp3` 各一份，
浏览器按 `canPlayType` 选其中一种加载（见 `web/src/sfx.ts`）。只做了格式转换与音量归一，没有二次创作。
总体积约 356 kB，按需懒加载，首次用户点击 / 按键之前不会创建 AudioContext，也不会发出任何声音。

| 游戏内用途 | 文件 | 原始素材包 | 原始文件名 |
|---|---|---|---|
| UI 点击 / 光标 | `click.ogg` / `click.mp3` | Interface Sounds | `select_002.ogg` |
| 对话翻页 | `tick.*` | Interface Sounds | `tick_001.ogg` |
| 确认 / 购买 / 装备 | `confirm.*` | Interface Sounds | `confirmation_001.ogg` |
| 取消 / 关闭 | `cancel.*` | Interface Sounds | `close_001.ogg` |
| 打开手记 / 商店 | `open.*` | Interface Sounds | `open_001.ogg` |
| 不能这么做 | `error.*` | Interface Sounds | `error_004.ogg` |
| 走一步 | `step.*` | Impact Sounds | `footstep_concrete_000.ogg` |
| 走一步（变体） | `step2.*` | Impact Sounds | `footstep_concrete_001.ogg` |
| 开箱 | `chest.*` | RPG Audio | `doorOpen_1.ogg` |
| 金币 | `coin.*` | RPG Audio | `handleCoins.ogg` |
| 换装备 | `equip.*` | RPG Audio | `clothBelt.ogg` |
| 挥砍 | `slash.*` | RPG Audio | `knifeSlice.ogg` |
| 命中 | `hit.*` | Impact Sounds | `impactPunch_medium_001.ogg` |
| 会心一击 | `crit.*` | Impact Sounds | `impactPunch_heavy_000.ogg` |
| 格挡 | `block.*` | Impact Sounds | `impactMetal_light_002.ogg` |
| 闪避 / 落空 | `miss.*` | RPG Audio | `cloth1.ogg` |
| 吟唱 / 法术 | `magic.*` | Interface Sounds | `glass_001.ogg` |
| 法术命中 | `magichit.*` | Impact Sounds | `impactGlass_medium_000.ogg` |
| 治疗 | `heal.*` | Music Jingles | `jingles_PIZZI16.ogg` |
| 倒下 | `ko.*` | Impact Sounds | `impactSoft_heavy_001.ogg` |
| 存档点 / 区域标题 | `bell.*` | Impact Sounds | `impactBell_heavy_000.ogg` |
| 升级 | `levelup.*` | Music Jingles | `jingles_PIZZI10.ogg` |
| 战斗胜利 | `victory.*` | Music Jingles | `jingles_PIZZI02.ogg` |
| 战斗失败 | `defeat.*` | Music Jingles | `jingles_PIZZI01.ogg` |
| 闪避（侧身的风声） | `evade.*` | RPG Audio | `bookFlip3.ogg` |
| 抵抗（法术在护壁上碎开） | `resist.*` | Impact Sounds | `impactGlass_light_003.ogg` |
| 获得增益状态 | `buff.*` | Interface Sounds | `pluck_002.ogg` |
| 被施加减益状态 | `debuff.*` | Interface Sounds | `question_004.ogg` |
| 火系法术释放 / 爆燃 | `fire.*` | Impact Sounds | `impactSoft_heavy_003.ogg` |
| 冰 / 晶系法术 | `ice.*` | Impact Sounds | `impactGlass_heavy_001.ogg` |
| 水 / 酸液 | `water.*` | Interface Sounds | `drop_002.ogg` |
| 雷击 | `bolt.*` | Impact Sounds | `impactPlate_heavy_001.ogg` |
| 风系 / 蒸汽 | `wind.*` | RPG Audio | `cloth3.ogg` |
| 地 / 岩系 | `earth.*` | Impact Sounds | `impactMining_002.ogg` |
| 暗 / 重力（低速播放） | `dark.*` | Impact Sounds | `impactBell_heavy_004.ogg` |
| 光系 | `chime.*` | Interface Sounds | `glass_004.ogg` |
| 护罩碎裂（boss 护罩被破解） | `shieldbreak.*` | Impact Sounds | `impactGlass_heavy_004.ogg` |
| 护罩重新罩上 | `shieldup.*` | Interface Sounds | `bong_001.ogg` |
| 操作机关（阀门 / 铃绳 / 秤盘） | `lever.*` | RPG Audio | `metalLatch.ogg` |
| 地形变化（落石 / 秤杆落下） | `rumble.*` | Impact Sounds | `impactMining_004.ogg` |

法术与反应的音效是 v3 加的，全部来自同样的四个 Kenney.nl CC0 包，用 `tools/build-sfx.py` 切条 / 归一化后
导出 `.ogg` + `.mp3`；每条的原始文件记在 `sfx/sources.json` 里。

没有背景音乐：没有找到合适的 CC0 原声吉他 / 室内乐轨，宁缺毋滥。

**明确没有使用**：RPG Maker RTP（任何版本）的音效或音乐。RTP 的授权仅限于在 RPG Maker 引擎内使用，
不能放进自己写的 web 引擎里。本项目的音频只有上面这一张表里的 CC0 文件。

## 美术（`art/web/`）

游戏内的背景、立绘、怪物、道具图标、头像 token 全部是本项目用图像模型生成后人工筛选的产物，
不是第三方素材，也没有描摹任何既有作品的角色。生成记录在 `art/prompts/`、`art/logs/`、`art/manifest.json`。

地块、单位底座、战斗特效（挥砍 / 火花 / 治疗 / 格挡）、浮动数字、UI 全部是 canvas / CSS 代码画的，
没有使用任何第三方图块或特效包。

## 字体

只使用系统字体栈（宋体 / Noto Serif CJK / Source Han Serif → serif，PingFang / Noto Sans CJK → sans-serif）。
没有内嵌或引用任何在线字体。

## 代码

引擎与前端为本项目原创（`engine/`、`web/src/`）。运行时零依赖；构建期只用 esbuild（MIT）与 Playwright（Apache-2.0）。
