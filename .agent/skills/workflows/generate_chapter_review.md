---
description: Generate comprehensive bilingual chapter review materials from textbook content
---

# Chapter Review Generation Workflow

Generate complete chapter review files for the Organizational Behavior course.

## Trigger

User says: "复习第X章" or "Create chapter review for Chapter X" or "为Ch{N}创建复习讲解"

## Steps

### 1. Identify Chapter

- Extract chapter number from user request
- Reference `.agent/skills/SKILL.md` for chapter theory mapping
- Determine priority level (⭐ rating)

### 2. Read Textbook Content

Locate chapter in textbook:
```
Path: 归档/课程指定教材/组织行为学精要 英文版·第14版14994789.md
```

Read the relevant sections and extract:
- Key definitions
- Theoretical frameworks
- Important examples
- Chapter summary
- Implications for managers

### 3. Generate Review File

Create file using the structure below:

```markdown
# Chapter X: [English Name] / [Chinese Name]

> **章节:** Chapter X  
> **教材:** Robbins & Judge, Essentials of OB (14th Edition)  
> **重要程度:** ⭐⭐⭐⭐⭐ (or as appropriate)

---

## 第一部分：理论基础 / Theory Foundations

[Complete theory explanations from textbook, bilingual]

---

## 第二部分：核心概念速查 / Core Concepts Quick Reference

### 术语词汇表 / Glossary

| 术语 / Term | 中文 | 定义 / Definition |
|------------|------|------------------|

### 理论对比表 / Comparison Tables

---

## 第三部分：考点总结 / Key Exam Points

### 🔴 高频考点（必考）
### 🟡 中频考点（常考）
### 🟢 低频考点（了解）

---

## 第四部分：复习卡片 / Review Cards

### 自测题 / Self-Test Questions

[8-12 practice questions covering: single choice, true/false, matching]

---

## 第五部分：考试策略 / Exam Strategy

### 单选题技巧
### 论述题答题模板

---

## 第六部分：中英文对照总结 / Bilingual Summary

---

> **复习建议 / Study Tips:**
```

### 4. Save File

```
Path: 期末复习/章节复习讲解/Ch{N}_{Chinese_Topic}.md
```

Example: `Ch1_OB导论.md`, `Ch2_工作态度.md`

### 5. Update Progress

Update the "Current Study Progress" table in `.agent/skills/SKILL.md` to reflect completion.

## Quality Requirements

- All theory explanations must start from zero (beginner-friendly)
- **BILINGUAL FORMAT IS MANDATORY**:
  - Every English paragraph MUST be followed by Chinese translation
  - All headings must be bilingual: `## 中文 / English`
  - Tables must have bilingual headers and content
  - Key points use blockquotes in both languages
  - Self-test answers use `<details>` tags with bilingual explanations
- Glossary must include ALL key terms from the chapter
- Self-test questions must cover all high-priority exam points (8-12 questions)
- Exam tips must be specific and actionable (keyword → answer patterns)
- File must be self-contained and comprehensive

## Bilingual Format Specification

See `.agent/skills/chapter-review-format.md` for complete format template.

**Key Rules:**
1. **正文格式 / Body Text**:
   ```
   [Complete English paragraph]
   
   [完整中文翻译]
   ```

2. **重点提示 / Key Points**:
   ```
   > **Key Point**: [English]  
   > **记忆要点**：[中文]
   ```

3. **表格 / Tables**:
   ```
   | 术语 / Term | 中文 | 定义 / Definition |
   |------------|------|------------------|
   | Term | 中文术语 | English definition (中文解释) |
   ```

4. **答案解析 / Answers**:
   ```
   <details>
   <summary>查看答案 / Answer</summary>
   **Answer:** [答案]
   **解析 / Explanation:** [中英双语]
   </details>
   ```

## Theory Reference

Use `.agent/skills/chapter-review-format.md` for chapter list and completed status.
