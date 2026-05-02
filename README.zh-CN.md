# clt-learning-skill

> 一个将**认知负荷理论(Cognitive Load Theory, CLT)**应用于学习材料设计、审视、重写与诊断的 skill。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-0.1.0-blue.svg)](CHANGELOG.md)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

**语言:** [English](README.md) · [繁體中文](README.zh-TW.md) · [简体中文](README.zh-CN.md)

提炼自 30 多年教育心理学原始文献 — Sweller (1988);Sweller、van Merriënboer & Paas (1998);van Merriënboer & Sweller (2005);de Jong (2010);Paas & van Merriënboer (2020)。

> ⚠️ **使用前须知。** CLT 是在人类课堂学习情境下被验证的。将其套用到由 AI 生成的材料是一个**合理但尚未经实证**的延伸推论。请把这个 skill 当作结构化的启发式准则,而不是保证有效的最佳化方案。详见 [`references/caveats.md`](references/caveats.md)。

---

## 这个 skill 做什么

载入后,它会协助 agent:

1. **GENERATE(生成)** — 产出符合工作记忆限制的学习笔记、样例、卡片、测验题目与课程结构。
2. **REVIEW(审视)** — 用 12 个经典 CLT 效应检视现有材料。
3. **REFACTOR(重写)** — 把材料改写成适合不同专业程度的版本(新手 ↔ 中等 ↔ 专家)。
4. **DIAGNOSE(诊断)** — 从内在负荷与外在负荷的角度,解释为何某一章节让人觉得吃力。

它**不会**产出整套内容库 — 它塑造的是 agent 在当下生成或评论教学内容的方式。

## 何时会触发

例如以下这类请求:

- *"帮我做 X 的学习笔记"*
- *"把这段改写成新手版本"*
- *"为什么这一章看起来特别吃力?"*
- 任何明确提到认知负荷、工作记忆、样例、注意力分散、形式效应或专家逆转效应的场合。

它**刻意不会**为一般写作、代码文档、营销文案,或单纯的资料查询而触发。

## 安装

### 作为项目级 skill

```bash
cd <your-project>
mkdir -p .claude/skills
git clone https://github.com/hhgaga/clt-learning-skill.git .claude/skills/clt-learning-skill
```

### 作为用户级 skill(所有项目)

```bash
git clone https://github.com/hhgaga/clt-learning-skill.git ~/.claude/skills/clt-learning-skill
```

这个 skill 采用标准的 `SKILL.md` 格式,任何支持该格式的 agent harness 都会自动发现它。重启 agent 后即可使用。

### 验证安装

向你的 agent 询问:

> *"用 CLT 帮我做 X 的新手学习笔记。"*

agent 应该会载入 `clt-learning-skill`,并说明它套用了哪些 CLT 效应。

## 目录结构

```
SKILL.md                              # 入口文件 + 决策流程
references/
  effects-catalog.md                  # 12 个经典 CLT 效应,含前后对照示例
  decision-trees.md                   # 专业程度 × 内在负荷 → 应用效应矩阵
  review-checklist.md                 # 19 点结构化审视流程
  learner-side-strategies.md          # 手势、合作等学习者端策略,已标注对 AI 场景未经验证
  caveats.md                          # de Jong 对相关负荷的批评 + AI 推论落差
  sources.md                          # 每个论点对应的原始论文
examples/
  generate-novice-notes.md            # GENERATE 示例输出
  review-existing-chapter.md          # REVIEW 示例输出
  diagnose-overwhelm.md               # DIAGNOSE 示例输出
ROADMAP.md                            # v0.1 → v1.0
CHANGELOG.md
CONTRIBUTING.md
LICENSE                               # MIT
```

## 设计原则

- **引用,不断言。** 每个论点都能追到 [`references/sources.md`](references/sources.md) 里的原始论文。
- **可被证伪,而非民间传说。** de Jong 对相关负荷(germane load)的批评会明确列出,不会被藏起来。
- **不读心。** 这个 skill 描述的是设计选择,而不是揣测使用者脑中发生了什么。
- **核心保持领域中立。** 领域特化的内容(例如 PT、数学、编程)以姊妹 skill 的形式发布。

## 版本管理

采用 Semver。v0.x 期间,触发描述与 reference 结构可能会有破坏性变更;v1.0 后公开接口才会冻结。详见 [`ROADMAP.md`](ROADMAP.md)。

## 引用

若这个 skill 对你的工作有帮助,可如下引用:

> hhgaga (2026). *clt-learning-skill* (v0.1.0) [skill]. https://github.com/hhgaga/clt-learning-skill

理论本身请引用 [`references/sources.md`](references/sources.md) 中的原始文献,不是这个 skill。

## 贡献

请见 [`CONTRIBUTING.md`](CONTRIBUTING.md)。欢迎 issue 与 PR,特别是:

- 推荐的效应实际反而变差的反例。
- 领域特化的样例。
- 引用错误的修正。

## 授权

[MIT](LICENSE)。
