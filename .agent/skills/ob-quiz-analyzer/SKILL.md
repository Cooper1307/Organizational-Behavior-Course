---
name: "ob-quiz-analyzer"
description: "Systematically analyzes OB chapters, quizzes, and case studies with theory foundations, bilingual explanations, and review cards. Invoke when user requests chapter review, quiz/case analysis, or exam preparation."
---

# 组织行为学Quiz与案例分析解析器

## 功能概述

本技能用于对组织行为学（Organizational Behavior）进行系统化复习和解析，包含三种模式：
1. **章节复习模式**: 从零开始讲解章节理论（理论基础+核心概念+复习卡片+自测题）
2. **Quiz解析模式**: 完整解析Quiz题目（理论基础+全题解析+复习卡片+考试策略）
3. **案例分析模式**: 双语分析组织案例（完整引用+理论应用+复习卡片）

## 触发条件

当用户提出以下需求时调用本技能：
- "复习第X章" / "Create chapter review for Chapter X"
- 解析Quiz文件（quiz1.md, quiz2.md, quiz3.md等）
- 分析案例文件（case study）
- 请求创建复习材料或考试准备
- 要求从零讲解理论基础知识
- 需要中英双语对照的学习材料

## 工作流程

### 模式一：章节复习讲解

#### 第一步：读取教材内容

从教材路径读取指定章节内容：
```
教材路径: 归档/课程指定教材/组织行为学精要 英文版·第14版14994789.md
```

#### 第二步：创建理论基础讲解

针对章节涉及的所有理论，创建完整的理论基础章节：

**理论基础讲解格式**

每个理论必须包含：

```markdown
## 理论名称 / Theory Name

**提出者/Proposed by:** 人名 (年份)

### 核心概念 / Core Concepts
- 要点1
- 要点2
- 要点3

### 公式/模型 / Formula/Model (if applicable)
```
公式说明
```

### 应用场景 / Application
- 何时使用此理论
- 如何应用于实际案例

### 中文讲解 / Chinese Explanation
（完整的中文理论讲解，适合零基础学习者）
```

#### 第三步：创建核心概念速查

包含：
- **术语词汇表 / Glossary**（所有重要术语的中英对照定义）
- **理论对比表 / Comparison Tables**（相关理论的对比）

#### 第四步：创建考点总结

按重要程度排序：
- 🔴 高频考点（必考）
- 🟡 中频考点（常考）
- 🟢 低频考点（了解）

#### 第五步：创建复习卡片

**1. 术语词汇表 / Glossary**

| 术语 / Term | 中文 | 定义 / Definition |
|------------|------|------------------|
| Term 1 | 中文1 | 简短定义 |

**2. 理论对比表 / Theory Comparison**

| 对比维度 | 理论A | 理论B |
|---------|-------|-------|
| 核心焦点 | ... | ... |
| 关键变量 | ... | ... |
| 适用场景 | ... | ... |

**3. 考点总结 / Key Exam Points**

**4. 自测题 / Self-Test Questions**

创建8-12道模拟题，覆盖本章核心考点，包含单选题、判断题、配对题。

```markdown
**Q1:** [题目]

<details>
<summary>查看答案</summary>
**Answer:** [答案]
**解析:** [简要解析]
</details>
```

#### 第六步：考试策略

```markdown
## 考试策略 / Exam Strategy

### 单选题技巧
1. 看到"关键词A" → 选"答案A"
2. 看到"关键词B" → 选"答案B"

### 论述题答题模板
**题目示例:** [示例题目]
**标准答案:** [4-5句话的标准答案模板]
```

### 模式二：Quiz文件解析

#### 第一步：识别文件类型

```
Quiz文件 → 提取章节信息（Ch1+Ch2, Ch4+Ch5, Ch7+Ch8）
```

#### 第二步：理论基础讲解

同模式一的第二步。

#### 第三步：题目系统解析

对每道题目按以下格式解析：

```markdown
### Question X [单选/判断/配对]

**题干:** [完整引用英文题干]

**用户答案:** [答案选项] ✅/❌

**正确答案:** [答案选项]

**解析/Analysis:**
[英文解析]

**中文解析:**
[中文详细解析]

**考点/Key Concept:** [关联的理论知识]
```

#### 第四步：复习卡片 + 考试策略 + 错题反思

同模式一的第五、六步，另加错题反思表格：

```markdown
## 错题反思 / Wrong Answer Review

| 题号 | 用户答案 | 正确答案 | 错误原因 | 改进策略 |
|------|---------|---------|---------|---------|
| QX | A | B | [原因] | [策略] |
```

### 模式三：案例分析

#### 第一步：完整引用案例

**必须完整引用题干和case描述**

#### 第二步：题目解析

```markdown
### Question X

**问题:** [完整引用英文问题]

**用户答案/分析:**
[英文分析段落]

**中文翻译:**
[中文翻译段落]

**涉及理论/Theories Used:** [列出使用的理论]
```

#### 第三步：理论基础讲解

在案例解析文件末尾添加完整的理论基础讲解（同模式一第二步）。

## 输出文件规范

### 文件命名

- **章节复习**: `Ch{N}_{主题关键词}.md` → 保存到 `期末复习/章节复习讲解/`
- **Quiz文件**: `Quiz{N}_Ch{X}_Ch{Y}_Analysis.md` → 保存到 `期末复习/复习材料/quiz/`
- **案例文件**: `{Case_Name}_Case_Analysis.md` → 保存到 `期末复习/复习材料/小组作业/解析/`

### 文件结构（章节复习）

```markdown
# Chapter X: [英文名] / [中文名]

> **章节:** Chapter X  
> **教材:** Robbins & Judge, Essentials of OB (14th Edition)  
> **重要程度:** ⭐⭐⭐⭐⭐

---

## 第一部分：理论基础 / Theory Foundations

（完整的理论讲解）

---

## 第二部分：核心概念速查 / Core Concepts Quick Reference

### 术语词汇表 / Glossary

### 理论对比表 / Comparison Tables

---

## 第三部分：考点总结 / Key Exam Points

### 🔴 高频考点（必考）

### 🟡 中频考点（常考）

### 🟢 低频考点（了解）

---

## 第四部分：复习卡片 / Review Cards

### 自测题 / Self-Test Questions

---

## 第五部分：考试策略 / Exam Strategy

---

## 第六部分：中英文对照总结 / Bilingual Summary

---

> **复习建议 / Study Tips:**
```

### 文件结构（Quiz解析）

```markdown
# Quiz{N} Analysis: Chapter {X} + {Y}

> **得分/Score:** X/XX (X%)  
> **日期/Date:** YYYY-MM-DD

---

## 第一部分：理论基础 / Theory Foundations

---

## 第二部分：题目解析 / Question Analysis

---

## 第三部分：复习卡片 / Review Cards

### 术语词汇表 / Glossary
### 理论对比表 / Theory Comparison
### 考点总结 / Key Exam Points
### 自测题 / Self-Test Questions

---

## 第四部分：考试策略 / Exam Strategy

---

## 第五部分：错题反思 / Wrong Answer Review
```

## 特殊要求

1. **双语输出:** 所有英文段落下方必须紧跟中文翻译
2. **完整引用:** 案例题必须完整引用题干和case描述
3. **零基础友好:** 理论基础讲解必须假设用户完全没有背景知识
4. **单文件保存:** 每个Quiz或案例的完整解析保存在一个Markdown文件内
5. **格式一致:** 严格遵循上述文件结构和格式规范
6. **教材对齐:** 章节复习必须基于教材实际内容

## 核心理论速查表

### 期望理论 / Expectancy Theory (Vroom, 1964)

三要素：
- **期望 (Expectancy):** 努力→绩效的可能性
- **工具性 (Instrumentality):** 绩效→奖励的可能性
- **效价 (Valence):** 奖励对个人的吸引力

激励力 = 期望 × 工具性 × 效价

### 公平理论 / Equity Theory (Adams, 1963)

核心：员工比较自己的投入产出比与他人的投入产出比

- 公平 = 我的产出/我的投入 = 他人的产出/他人的投入
- 不公平会导致行为调整（减少努力、要求加薪、离职等）

### 强化理论 / Reinforcement Theory (Skinner)

- **正强化:** 给予奖励以增加行为频率
- **负强化:** 移除厌恶刺激以增加行为频率
- **惩罚:** 给予厌恶刺激以减少行为频率
- **消退:** 不给予任何反应以减少行为频率

### 目标设置理论 / Goal-Setting Theory (Locke, 1968)

具体且困难的目标 + 反馈 = 更高绩效

### 马斯洛需求层次 / Maslow's Hierarchy

生理 → 安全 → 社交 → 尊重 → 自我实现

### 双因素理论 / Two-Factor Theory (Herzberg)

- **保健因素 (Hygiene):** 防止不满，但不激励
- **激励因素 (Motivators):** 真正激励员工

### 工作特征模型 / Job Characteristics Model (JCM)

五大核心维度：
1. 技能多样性 (Skill Variety)
2. 任务同一性 (Task Identity)
3. 任务重要性 (Task Significance)
4. 自主性 (Autonomy) ⭐
5. 反馈 (Feedback) ⭐

**MPS公式:**
```
MPS = [(SV + TI + TS) / 3] × Autonomy × Feedback
```

> ⭐ Autonomy和Feedback是相乘因素，影响最大

## 17章理论映射表

| 章节 | 核心理论 |
|------|---------|
| Ch1 | OB定义、三大决定因素、Luthans管理活动、OB模型 |
| Ch2 | 态度三成分、认知失调、EVLN模型、工作满意度、POS |
| Ch3 | 情绪vs心境、情绪劳动、AET理论、情绪智力 |
| Ch4 | MBTI、Big Five (OCEAN)、CSE、人-职匹配 |
| Ch5 | 归因理论、知觉偏差、决策模型、创造性 |
| Ch6 | 生物特征、能力、多样性管理 |
| Ch7 | 马斯洛、双因素、麦克利兰、期望理论、公平理论、目标设置、强化理论 |
| Ch8 | JCM模型、MPS公式、工作设计、薪酬激励、福利 |
| Ch9 | 沟通过程、沟通方向、小道消息、沟通障碍 |
| Ch10 | 群体发展阶段、角色、规范、地位、规模、凝聚力 |
| Ch11 | 团队类型、团队建设、团队有效性、信任 |
| Ch12 | 特质理论、行为理论、权变理论、变革型领导、信任 |
| Ch13 | 权力来源、依赖性、印象管理、政治行为 |
| Ch14 | 冲突过程、冲突处理意图、谈判策略 |
| Ch15 | 工作专门化、部门化、管理幅度、矩阵结构 |
| Ch16 | 文化特征、文化创建与保持、文化影响 |
| Ch17 | Lewin三阶段模型、变革阻力、组织发展 |

## 使用示例

**用户输入:** "复习第1章"

**执行步骤:**
1. 读取教材Ch1内容
2. 创建理论基础讲解（OB定义、三层次模型、成功vs有效管理者）
3. 创建核心概念速查（术语表、对比表）
4. 创建考点总结
5. 创建复习卡片（术语表、对比表、考点、8-12道自测题）
6. 提供考试策略
7. 保存为 `Ch1_OB导论.md`

**用户输入:** "解析quiz1.md"

**执行步骤:**
1. 读取quiz1.md文件内容
2. 识别涉及章节（如Ch1+Ch2）
3. 根据章节确定需要讲解的理论
4. 创建理论基础讲解部分
5. 逐题解析，提供中英双语解析
6. 创建复习卡片（术语表、对比表、考点、自测题）
7. 提供考试策略和错题反思
8. 保存为 `Quiz1_Ch1_Ch2_Analysis.md`
