# Workflow: Parse Textbook Paragraph (精读原版教材)

> **触发方式**: `/parse_textbook` 或用户提供一个英文原文段落并要求解析

---

## Overview

本 workflow 用于对 Robbins & Judge *Organizational Behavior* 原版教材段落进行**系统性、多维度的精读分析**，输出格式统一，适合课程学习、笔记整理和备考使用。

---

## Step 1 — 接收原文

用户提供：
- 教材章节编号（如 Chapter 7）
- 段落原文（英文）

如用户未提供章节信息，询问后继续。

---

## Step 2 — 输出解析

按照 `rules.md` 中的 **Textbook Paragraph Analysis Template** 逐项输出，顺序如下：

1. `📄 原文` — 原版英文段落（原样保留，不修改）
2. `🌐 中文翻译` — 学术中文全文翻译，忠实原意，不意译过度
3. `📝 段落精要 (Summary)` — 3–5句话提炼段落核心观点，中英双语
4. `🔍 词汇深度解析 (Vocabulary Deep Dive)` — 对段落中**每一个**重要词汇/短语单独展开分析（见模板）
5. `🧠 句式与修辞分析 (Syntax & Rhetoric)` — 分析段落的句型结构、论证逻辑、修辞策略
6. `🔗 理论定位 (Theory Mapping)` — 将段落内容锚定到具体 OB 理论框架（含章节、作者、年代）
7. `⚠️ 考点提炼 (Exam Focus)` — 标出可能出现在考题中的核心概念和定义
8. `💡 延伸思考 (Critical Thinking)` — 提出1–2个开放性问题，连接现实案例

---

## Step 3 — 文件存储（可选）

如用户需要保存，按以下规范命名并存储：

```
组织行为学/
└── chapter_notes/
    └── Ch{章号}_{主题关键词}_paragraph_analysis.md
```

例如：`Ch07_Motivation_expectancy_theory_paragraph_analysis.md`

---

## Notes

- 词汇解析数量：每段优先分析 **3–8 个**高价值词汇（频率低但意义重、学术专业词、OB 术语优先）
- 翻译风格：学术书面语，避免口语化
- 母语者语感部分用**第一人称**描述，模拟英语母语者的直觉反应
