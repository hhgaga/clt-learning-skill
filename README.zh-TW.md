# clt-learning-skill

> 一個將**認知負荷理論(Cognitive Load Theory, CLT)**應用於學習教材設計、審視、重寫與診斷的 skill。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-0.1.0-blue.svg)](CHANGELOG.md)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

**語言:** [English](README.md) · [繁體中文](README.zh-TW.md) · [简体中文](README.zh-CN.md)

提煉自 30 多年教育心理學原始文獻 — Sweller (1988);Sweller、van Merriënboer & Paas (1998);van Merriënboer & Sweller (2005);de Jong (2010);Paas & van Merriënboer (2020)。

> ⚠️ **使用前須知。** CLT 是在人類課堂學習情境下被驗證的。將其套用到由 AI 生成的教材是一個**合理但尚未經實證**的延伸推論。請把這個 skill 當作結構化的啟發式準則,而不是保證有效的最佳化方案。詳見 [`references/caveats.md`](references/caveats.md)。

---

## 這個 skill 做什麼

載入後,它會協助 agent:

1. **GENERATE(生成)** — 產出符合工作記憶限制的學習筆記、樣例、字卡、測驗題目與課程結構。
2. **REVIEW(審視)** — 用 12 個經典 CLT 效應檢視現有教材。
3. **REFACTOR(重寫)** — 把教材改寫成適合不同專業程度的版本(新手 ↔ 中等 ↔ 專家)。
4. **DIAGNOSE(診斷)** — 從內在負荷與外在負荷的角度,解釋為何某一章節讓人覺得吃力。

它**不會**產出整套內容庫 — 它形塑的是 agent 在當下生成或批評教學內容的方式。

## 何時會觸發

例如以下這類請求:

- *「幫我做 X 的學習筆記」*
- *「把這段改寫成新手版本」*
- *「為什麼這一章看起來特別吃力?」*
- 任何明確提到認知負荷、工作記憶、樣例、注意力分散、形式效應或專家逆轉效應的場合。

它**刻意不會**為一般寫作、程式碼文件、行銷文案,或單純的資料查詢而觸發。

## 安裝

### 作為專案層級 skill

```bash
cd <your-project>
mkdir -p .claude/skills
git clone https://github.com/hhgaga/clt-learning-skill.git .claude/skills/clt-learning-skill
```

### 作為使用者層級 skill(所有專案)

```bash
git clone https://github.com/hhgaga/clt-learning-skill.git ~/.claude/skills/clt-learning-skill
```

這個 skill 採用標準的 `SKILL.md` 格式,任何支援該格式的 agent harness 都會自動發現它。重啟 agent 之後即可使用。

### 驗證安裝

向你的 agent 詢問:

> *「用 CLT 幫我做 X 的新手學習筆記。」*

agent 應該會載入 `clt-learning-skill`,並說明它套用了哪些 CLT 效應。

## 目錄結構

```
SKILL.md                              # 入口檔 + 決策流程
references/
  effects-catalog.md                  # 12 個經典 CLT 效應,含前後對照範例
  decision-trees.md                   # 專業程度 × 內在負荷 → 應用效應矩陣
  review-checklist.md                 # 19 點結構化審視流程
  learner-side-strategies.md          # 手勢、合作等學習者端策略,已標註對 AI 場景未經驗證
  caveats.md                          # de Jong 對相關負荷的批評 + AI 推論落差
  sources.md                          # 每個論點對應的原始論文
examples/
  generate-novice-notes.md            # GENERATE 範例輸出
  review-existing-chapter.md          # REVIEW 範例輸出
  diagnose-overwhelm.md               # DIAGNOSE 範例輸出
ROADMAP.md                            # v0.1 → v1.0
CHANGELOG.md
CONTRIBUTING.md
LICENSE                               # MIT
```

## 設計原則

- **引用,不斷言。** 每個論點都能追到 [`references/sources.md`](references/sources.md) 裡的原始論文。
- **可被否證,而非民間傳說。** de Jong 對相關負荷(germane load)的批評會明確列出,不會被藏起來。
- **不讀心。** 這個 skill 描述的是設計選擇,而不是揣測使用者腦中發生了什麼。
- **核心保持領域中立。** 領域特化的內容(例如 PT、數學、程式設計)以姊妹 skill 的形式發布。

## 版本管理

採用 Semver。v0.x 期間,觸發描述與 reference 結構可能會有破壞性變更;v1.0 後公開介面才會凍結。詳見 [`ROADMAP.md`](ROADMAP.md)。

## 引用

若這個 skill 對你的工作有幫助,可如下引用:

> hhgaga (2026). *clt-learning-skill* (v0.1.0) [skill]. https://github.com/hhgaga/clt-learning-skill

理論本身請引用 [`references/sources.md`](references/sources.md) 中的原始文獻,不是這個 skill。

## 貢獻

請見 [`CONTRIBUTING.md`](CONTRIBUTING.md)。歡迎 issue 與 PR,特別是:

- 推薦的效應實際反而變差的反例。
- 領域特化的樣例。
- 引用錯誤的修正。

## 授權

[MIT](LICENSE)。
