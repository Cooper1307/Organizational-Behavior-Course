---
description: Generate exam review materials for a specified range of OB chapters
---

# OB Exam Review Workflow

Use this workflow to generate comprehensive review materials for exam preparation.

## Steps

1. **Confirm the scope** — which chapters or topics the user wants to review (e.g., "Ch. 3-8" or "Individual Behavior section").

2. **Generate a Knowledge Summary** for each chapter in scope:
   - Chapter title (English + Chinese)
   - 3-5 key concepts with brief definitions
   - Most important theory/model with a diagram description
   - Common exam question types for this chapter

3. **Create a Theory Comparison Table** for related theories:

   ```
   | Theory | Theorist | Year | Focus | Key Idea | Limitation |
   |--------|----------|------|-------|----------|------------|
   | ... | ... | ... | ... | ... | ... |
   ```

4. **Generate practice questions** (aim for 2-3 per chapter):
   - **Definitions**: "Define [term] and explain its relevance to OB."
   - **Short Answer**: "Compare and contrast Theory A and Theory B."
   - **Essay/Case**: "Apply [theory] to analyze the following scenario: ..."
   - **True/False** with explanations

5. **Provide model answers** for each practice question:
   - Structured in the exam-friendly format: Introduction → Main Points → Conclusion
   - Include key terms in **bold** with Chinese translations

6. **Create an "易混淆概念" (Easily Confused Concepts) section**:
   - List pairs of similar concepts that students often confuse
   - Explain the differences clearly

7. **Save the output** to `review/Review_Ch_XX-XX.md` (create `review/` folder if it doesn't exist).

## Example Trigger

User says: "帮我复习第3到8章" or "Review Chapters 3-8 for the exam"
