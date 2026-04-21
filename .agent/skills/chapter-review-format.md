# 章节复习文件双语格式规范 / Bilingual Format Specification

## 语言要求 / Language Requirements

**主要语言**: 英文（考试语言）
**辅助语言**: 中文（每个英文段落下方必须配有中文翻译）
**原因**: 用户英文不是特别好，需要中文辅助理解

---

## 文件结构模板 / File Structure Template

```markdown
# Chapter {N}: {English Topic} / {Chinese Topic}

> **章节:** Chapter {N}  
> **教材:** Robbins & Judge, Essentials of Organizational Behavior (14th Edition)  
> **重要程度:** ⭐⭐⭐⭐⭐/⭐⭐⭐⭐/⭐⭐⭐

---

## 第一部分：理论基础 / Theory Foundations

### 一、{Topic Name} / {English Topic Name}

[English paragraph - complete explanation in English]

[中文翻译 - 下方紧跟完整的中文翻译]

> **Key Point**: [英文关键点]  
> **记忆要点**：[中文翻译]

### 二、{Next Topic} / {English Name}

[Same bilingual format...]

---

## 第二部分：核心概念速查 / Core Concepts Quick Reference

### 术语词汇表 / Glossary

| 术语 / Term | 中文 | 定义 / Definition |
|------------|------|------------------|
| Term | 中文术语 | English definition (中文解释) |

### 理论对比表 / Comparison Tables

[Tables with bilingual headers and content]

---

## 第三部分：考点总结 / Key Exam Points

### 🔴 高频考点（必考）
1. **[Concept]**: English explanation (中文解释)

### 🟡 中频考点（常考）

### 🟢 低频考点（了解）

---

## 第四部分：复习卡片 / Review Cards

### 自测题 / Self-Test Questions

#### 单选题 / Multiple Choice

**Q1:** [Question in English]

A. [Option A]
B. [Option B]
C. [Option C]
D. [Option D]

<details>
<summary>查看答案 / Answer</summary>

**Answer:** [Letter]

**解析 / Explanation:** [中英双语解析]

</details>

#### 判断题 / True or False

**Q2:** [Statement in English] (T/F)

<details>
<summary>查看答案 / Answer</summary>

**Answer:** [True/False]

**解析 / Explanation:** [中英双语解析]

</details>

#### 配对题 / Matching

**Q3:** Match the following:

<details>
<summary>查看答案 / Answer</summary>

**Answer:** 1-A, 2-B, 3-C

**解析 / Explanation:** [中英双语解析]

</details>

---

## 第五部分：考试策略 / Exam Strategy

### 单选题技巧 / Tips for Multiple Choice

1. See "[keyword]" → Choose **[Concept]**
   看到"[关键词]" → 选 **[概念]**

### 论述题答题模板 / Essay Answer Template

**题目示例 / Sample Question:** [English question]

**标准答案 / Standard Answer:**

1. [First point in English]
   
   [第一点中文翻译]

2. [Second point in English]
   
   [第二点中文翻译]

---

## 第六部分：中英文对照总结 / Bilingual Summary

| 英文 / English | 中文 / Chinese |
|---------------|----------------|
| Key concept 1 | 关键概念1 |
| Key concept 2 | 关键概念2 |

---

> **复习建议 / Study Tips:**
> 1. [English instruction]
>    [中文翻译]
> 2. [English instruction]
>    [中文翻译]
```

---

## 格式规范 / Formatting Rules

### 1. 标题规范 / Heading Rules

- 所有标题必须双语：`## 中文 / English` 或 `### 中文 / English`
- 章节标题格式：`# Chapter {N}: {English Topic} / {Chinese Topic}`

### 2. 正文格式 / Body Text Format

**先英文，后中文**：
```markdown
[Complete English paragraph explaining the concept]

[完整的中文翻译段落]
```

**示例 / Example**:
```markdown
Emotions are intense feelings that are directed at someone or something. They are short-lived and have a clear cause.

情绪是针对特定对象或事件的强烈感受，持续时间较短（通常几秒到几分钟），且有明确的触发原因。
```

### 3. 表格格式 / Table Format

**列标题双语**：
```markdown
| 术语 / Term | 中文 | 定义 / Definition |
```

**单元格内容**：
```markdown
| Term | 中文术语 | English definition (中文解释) |
```

### 4. 重点提示 / Key Points

使用blockquotes突出关键点：
```markdown
> **Key Point**: [English explanation]  
> **记忆要点**：[中文解释]
```

### 5. 答案解析格式 / Answer Format

使用折叠标签：
```markdown
<details>
<summary>查看答案 / Answer</summary>

**Answer:** [答案]

**解析 / Explanation:** [中英双语解析]

</details>
```

### 6. 复习建议 / Study Tips

双语对照列表：
```markdown
> **复习建议 / Study Tips:**
> 1. [English instruction]
>    [中文翻译]
> 2. [English instruction]
>    [中文翻译]
```

---

## 已完成的章节 / Completed Chapters

| 章节 / Chapter | 文件 / File | 状态 / Status |
|---------------|------------|---------------|
| Ch1 | Ch1_OB导论.md | ✅ 双语格式 |
| Ch2 | Ch2_工作态度.md | ✅ 双语格式 |
| Ch3 | Ch3_情绪.md | ✅ 双语格式 |

## 待创建的章节 / Pending Chapters

| 章节 / Chapter | 文件 / File | 优先级 / Priority |
|---------------|------------|------------------|
| Ch4 | Ch4_人格因素.md | ⭐⭐⭐⭐⭐ |
| Ch5 | Ch5_知觉与决策.md | ⭐⭐⭐⭐⭐ |
| Ch6 | Ch6_多元化.md | ⭐⭐⭐⭐ |
| Ch7 | Ch7_基础动机.md | ⭐⭐⭐⭐⭐ |
| Ch8 | Ch8_动机应用.md | ⭐⭐⭐⭐⭐ |
| Ch9 | Ch9_沟通.md | ⭐⭐⭐⭐ |
| Ch10 | Ch10_群体基础.md | ⭐⭐⭐⭐ |
| Ch11 | Ch11_团队.md | ⭐⭐⭐⭐ |
| Ch12 | Ch12_领导力.md | ⭐⭐⭐⭐⭐ |
| Ch13 | Ch13_权力与政治.md | ⭐⭐⭐⭐ |
| Ch14 | Ch14_冲突管理.md | ⭐⭐⭐⭐⭐ |
| Ch15 | Ch15_组织结构.md | ⭐⭐⭐ |
| Ch16 | Ch16_组织文化.md | ⭐⭐⭐ |
| Ch17 | Ch17_组织变革.md | ⭐⭐⭐ |
