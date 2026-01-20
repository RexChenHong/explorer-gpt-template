Explorer GPT Template

Explorer GPT 探索模板

A low-token, multi-model workflow for exploring large open-source repositories
一套低 token、多模型協作的大型開源專案探索流程
without requiring a software engineering background.
不需要具備軟體工程或資工背景即可使用。

What is this?
這是什麼？

This repository contains a methodology template for using multiple LLMs
本儲存庫提供一套方法論模板，用於協調多個大型語言模型（LLMs）
(low-cost models + high-end models) to explore GitHub repositories
（低成本模型 + 高階模型）來探索 GitHub 開源專案
in a cost-efficient and structured way.
並以結構化、節省 token 成本的方式進行分析。

It is specifically designed for:
此模板特別為以下族群設計：

People without a CS / software background
沒有資工或軟體工程背景的人

People who cannot read English technical documents well
不擅長閱讀英文技術文件的人

Individual developers building quantitative trading systems or other
正在開發量化交易系統或其他
data-heavy systems, who want to learn from large open-source projects
高資料量系統、希望從大型開源專案中學習
(like vn.py, Polars, etc.) without copying code and without burning
（如 vn.py、Polars 等），但不想直接複製程式碼**、也不想大量燒 token
huge amounts of tokens**.

This is a one-time snapshot of a workflow that was validated in practice.
這是一份經過實際驗證的一次性流程快照。
It is not meant to be a long-term maintained framework.
它並非設計為長期維護的框架或產品。

```markdown
## Repository structure  
## 專案結構

```text
explorer-gpt-template/
├── README.md                    # This file (English introduction)
│                               # 本檔（英文介紹）
├── README_zh-TW.md              # Traditional Chinese introduction
│                               # 繁體中文介紹
├── EXPLORER_GPT.md              # Core methodology: Explorer GPT workflow
│                               # 核心方法論：Explorer GPT 探索流程
├── LICENSE                      # MIT License
│                               # MIT 授權
└── examples/
    ├── Polars_Design_Pattern_Analysis.md
    └── Polars_High_Level_Design_Evaluation.md
核心流程文件

The core workflow: roles, phases, rules, and prompts for Explorer GPT.
此文件定義 Explorer GPT 的核心流程：角色分工、階段、規則與提示語。

It defines how to:
它說明如何：

Start from a GitHub repo URL
從 GitHub 開源專案網址開始

Use terminal commands to inspect the repo (0 tokens)
使用終端機指令檢視專案結構（不消耗 token）

Use a low-tier model to extract design patterns and habits (cheap)
使用低階模型萃取設計模式與工程習慣（低成本）

Use a high-end model only on summaries, not on raw code (expensive)
僅讓高階模型閱讀摘要，而非原始碼（控制高成本）

Freeze useful results into agent skills / permanent rules
將有價值的結論固化為 agent skills 或長期規範

examples/polars_low_tier_extraction.md
Polars 低階模型探索範例

A real-world example of low-tier model exploration on the Polars project.
一份真實的 Polars 專案低階模型探索範例。
It shows what a “good” low-tier extraction output can look like.
用來示範「合理且足夠」的低階模型萃取結果應該長什麼樣子。

examples/polars_high_tier_evaluation.md
Polars 高階模型評估範例

A real-world example of high-end model evaluation of those extracted patterns,
一份高階模型對前述萃取結果進行評估的真實範例，
turning them into general design rules and trade-offs
並將其轉化為通用的設計原則與取捨判斷，
suitable for a personal system.
適合應用於個人系統或專案中。

What this is NOT
這不是什麼？

This repository is NOT:
本儲存庫不是：

A tutorial for Polars, vn.py, or any specific project
Polars、vn.py 或任何特定專案的教學

A code library or framework
程式碼函式庫或框架

A replacement for proper engineering or architecture work
正規工程設計或系統架構工作的替代品

A promise that following this workflow will produce “correct” or “optimal” systems
保證照做就能產生「正確」或「最佳化」系統的承諾

It is a thinking scaffold:
它是一個思考支架：
a way to talk to LLMs in a structured, low-cost manner
一種以結構化、低成本方式與大型語言模型互動的方法，
when exploring large repos.
用於探索大型開源專案。

Usage: how to use this template
使用方式

Read EXPLORER_GPT.md to understand the roles and phases.
先閱讀 EXPLORER_GPT.md，理解角色分工與各階段流程。

Take the examples/polars_.md files as reference output:
將 examples/polars_.md 視為「參考輸出結果」：

Use them to calibrate what your low-tier and high-tier prompts should produce.
用來校準低階與高階模型輸出應該達到的深度與範圍。

For your own target repo:
套用到你自己的目標專案時：

Start from the GitHub URL
從 GitHub 專案網址開始

Follow the “Phase 1 / Phase 2 / Phase 3 …” flow in EXPLORER_GPT.md
依照 EXPLORER_GPT.md 中的 Phase 1 / Phase 2 / Phase 3 流程執行

Replace Polars with your target project
將 Polars 換成你的目標專案

Optionally, adapt the final design rules into your own agent skills / system rules
視需要將最終規範轉化為你自己的 agent skills 或系統規則

Scope and disclaimer
範圍與免責聲明

This is a snapshot of a working workflow at one point in time.
這是一份在特定時間點可行的流程快照。
It does not track upstream changes in Polars or any other project.
不會追蹤 Polars 或其他專案的後續版本變化。

The examples are meant to illustrate the workflow,
範例僅用於示範探索流程本身，
not to describe the latest internals of those projects.
並非用來描述專案的最新內部實作。

You are responsible for evaluating and adapting these ideas to your own system.
如何採用與調整，需由使用者自行評估並承擔風險。

License
授權

MIT – see LICENSE for details.
MIT 授權，詳見 LICENSE 檔案。
