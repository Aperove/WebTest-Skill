# webtest-jp — 日本 Webテスト 备考·核对 Skill

一个 Claude Code Skill，帮助求职者**备考日本企业招聘网测**：识别题型、核对答案、查看中文解题过程、制定备考计划。

- **题目**保留日文原文；**解析**用中文。
- 支持文字题与**截图题**（视觉识别）。
- 覆盖全部主流测试：**SPI3 / 玉手箱 / GAB·C-GAB / CAB·Web-CAB / TG-WEB / SCOA / 性格检查** 等。

> 定位：自我备考与「答え合わせ（对答案）」的练习辅助工具——帮你把解法练熟、提速、补弱项。

## 怎么用

进入一轮（贴来一批题）时，助手会先问你这一轮要 **①只核对答案** 还是 **②附中文解题过程**，然后据此输出。说"换一批 / 新的一轮"会重新询问。

示例：
- "这几道玉手箱四則逆算帮我对下答案"（贴文字或截图）
- "这题 SPI 推論怎么解？用中文讲一下"
- "帮我排一个两周的 SPI 备考计划，重点非言語"

## 安装

作为 Claude Code Skill 使用，把本仓库放到 skills 目录下（文件夹名即 skill 名）：

```bash
git clone <this-repo> ~/.claude/skills/webtest-jp
```

或在项目内 `.claude/skills/webtest-jp/`。之后在对话里自然描述需求即可触发，或用 `/webtest-jp`（若环境支持斜杠调用）。

## 目录结构

```
SKILL.md                    # 入口：工作流 + 测试/题型路由 + 输出规范
references/                 # 各测试「判型 + 题型清单 + 出题形式」
  spi.md  tamatebako.md  gab-cab.md  tg-web.md  scoa-others.md
  personality.md  company-map.md
solutions/                  # 各题型「最快解法」模板
  spi-nonverbal.md  spi-verbal.md  tamatebako.md  cab.md
  tg-web.md  calc-shortcuts.md
assets/answer-format.md     # 答案核对 / 详解 输出模板
```

## 说明

- 本工具用于**备考练习与对答案**。请在符合各招聘方规则的前提下使用。
- "哪家公司用哪种测试"每年会变动，`references/company-map.md` 仅供参考，务必结合最新的过去问 / 口コミ 自行确认。
- 内容持续完善中：SPI 与玉手箱解法最完整，其余测试以"判型 + 题型清单 + 主解法"为主，细节逐步补充。
