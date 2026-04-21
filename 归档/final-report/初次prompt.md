[text](<d:/MyData/Download/Edge/2025年12月8日~/Final Report and Presentation Guidelines for Organizational Behavior_English dept..pdf>)
结合最新的网络搜索结果，我先为你简单梳理一下 **“AI Deep Research（深度研究）”** 功能的核心特点，然后再针对你的《组织行为学（OB）》期末报告，为你独家定制一套 Prompt。

### 1. 什么是 AI 的 Deep Research 功能？

目前，OpenAI（内置于 ChatGPT Pro，由 o3 模型驱动）、Google（Gemini Advanced）以及部分学术AI工具（如 Perplexity, Scopus AI）都推出了 Deep Research 功能。它与普通 AI 问答有本质区别：

* **自主的 Agent（智能体）行为**：普通的 AI 是“你问我答”；而 Deep Research 像一个不知疲倦的实习生。它会自己拆解任务、制定搜索计划、在后台连续自动进行几十次网页搜索。
* **超长篇幅与真实引用**：它会花 5 到 30 分钟去阅读上百个网页、PDF 和研报，然后生成带有**真实参考文献（Citations）**的万字长文，极大减少了 AI “幻觉”。
* **逻辑推理与交叉比对**：它能够将多个来源的信息进行结构化整合（比如同时对比多篇学术论文中的 OB 理论，并与某公司的实际情况结合）。

---

### 2. 针对你这份 OB 报告的“痛点”分析

仔细阅读你的作业要求后，我发现这是一个 **Field Study（实地调研）**。
**核心矛盾在于：** AI 可以在网上查阅海量资料，但 AI **无法代替你在线下真正去采访上海某公司的员工和发放问卷**。

因此，如果我们让 Deep Research 来写这份报告的“初稿”，我们的策略应该是**“半真半假，搭好框架”**：

1. **真实部分（让 AI 发挥强项）**：让 AI 找一家真实的上海中小企业（SME），深度挖掘该公司的公开背景、组织架构；同时让 AI 检索真实的组织行为学（OB）学术文献和理论。
2. **模拟部分（为你提供模板）**：让 AI **“模拟/编造”** 一份符合逻辑的问卷数据、访谈记录和图表占位符。你拿到初稿后，只需要带着 AI 设计好的问卷去实地调研，然后把真实数据替换掉 AI 模拟的数据即可。

---

### 3. Deep Research 专属 Prompt 设计

因为 Deep Research 运行时间长，且你的作业是全英文的，**Prompt 必须用英文撰写，并且要像一份详细的“项目任务书（Project Brief）”一样给它设定极其严格的框架。**

你可以直接复制以下 Prompt（括号内的内容你可以根据实际情况修改）：

***

#### ✂️ 请复制以下 Prompt 喂给带有 Deep Research 功能的 AI

**[Role & Mission]**
You are an expert research analyst and an A+ student in Organizational Behavior (OB). I need you to use your Deep Research capabilities to conduct a comprehensive multi-step investigation and generate a highly detailed first draft of an OB field study report.

**[Target Subject]**
* **Company:** Please select a REAL small or medium-sized enterprise (SME) based in Shanghai (e.g., a local tech startup, a boutique consulting firm, or a specialized manufacturing company). If I haven't specified one, please pick one that has sufficient public information and confirm its name and industry.
* **Key OB Topics:** Focus strictly on TWO topics for this report: **1. Motivation** and **2. Leadership Behavior and Power**.

**[Research Trajectory & Tasks]**
Please execute the following research steps:

1. **Background Search:** Scour the web for real information regarding the chosen Shanghai SME's history, products, organizational structure, and culture.
2. **Literature Review:** Find credible, recent academic sources or business articles explaining the theories behind "Motivation" (e.g., Maslow, Herzberg, Expectancy Theory) and "Leadership" (e.g., Transformational leadership, power dynamics) as they apply to SMEs.
3. **Data Simulation (Crucial):** Since this is a field study requiring first-hand data, please **SIMULATE** highly realistic primary data. Create hypothetical survey results (for 30 employees) and quotes from 2 hypothetical management interviews. Ensure these simulated issues perfectly bridge the real company background with the OB theories.
4. **Draft Generation:** Write the 10-12 page draft (approx. 3000 words) using the exact structure below.

**[Strict Report Structure]**
Generate the output using markdown, strictly following these headings:

1. **Title Page:** (Create a creative title, leave placeholders for group members, Date: June 14, 2024)
2. **Table of Contents**
3. **Introduction:** Introduce the SME and the purpose of this OB study.
4. **Company Background:** Detailed real information about the industry, size, and products.
5. **Organizational Overview:** Describe its structure and culture based on your research.
6. **Employee Background:** Discuss demographics and roles (Use simulated realistic data).
7. **Key OB Topics:** Provide academic context for Motivation and Leadership Behavior.
8. **Data Presentation and Analysis:** Present the simulated data. Use markdown tables to show survey results. Explicitly write "[Insert Pie Chart Here: Showing X]" as placeholders for visual aids.
9. **Discussion:** Analyze the simulated findings in the context of the OB theories researched in Step 2. What are the company's OB problems?
10. **Conclusion:** Summarize key findings and provide 3 actionable implications/recommendations for the company.
11. **References:** Provide REAL verifiable APA citations for the OB theories and company background information you found online. Do not hallucinate URLs.
12. **Appendices:**
    * Appendix A: Generate a complete 10-15 question OB survey (from general to specific, covering Motivation and Leadership).
    * Appendix B: Generate a mock interview transcript with a manager.

**[Guardrails]**
* **Tone:** Academic, professional, and objective.
* **Formatting constraint:** Ensure it's clear where the "Real Internet Research" ends and the "Simulated Field Data" begins. Mark the simulated sections clearly so I can replace them with my own real survey data later.

***

### 💡 这套 Prompt 为什么能完美适配 Deep Research？

1. **防偏航机制**：明确指定了 12 个部分的标题和顺序，防止 AI 在长达十几分钟的推理中跑题。
2. **利用了它的“联网检索”强项**：要求在 `References` 部分提供**真实的 APA 引用**，Deep Research 会认真去查阅文献库和企业官网，帮你把最痛苦的文献回顾（Literature Review）和企业背景调查直接做完。
3. **闭环了“调研作业”逻辑**：明确告诉 AI 去“伪造/模拟”核心数据（Data Simulation），并要求它直接生成 Appendix 里的问卷。这样你拿到初稿后：
   * 背景介绍、理论框架、排
