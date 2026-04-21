---
description: Generate a bilingual OB vocabulary list for a given chapter or topic
---

# OB Vocabulary Study Workflow

Use this workflow when studying OB terminology for a specific chapter or topic.

## Steps

1. **Identify the topic or chapter** the user wants to study (e.g., "Chapter 7 Motivation" or "Leadership theories").

2. **Extract key terms** from the chapter/topic. For each term, generate a Vocabulary Card using the template from `rules.md`:

   ```
   ## [English Term] (中文翻译)
   - **Definition**: Academic definition from the textbook
   - **Example Sentence**: A sentence using the term in an OB context
   - **Related Theory**: Which OB theory/framework it belongs to
   - **Contrast With**: Similar or opposite terms
   ```

3. **Organize the vocabulary list** by grouping related terms together (e.g., all motivation-related terms together).

4. **Save the output** to `vocab/Chapter_XX_Vocabulary.md` (create the `vocab/` folder if it doesn't exist).

5. **Generate a quick-review quiz** at the end of the file:
   - 5 English → Chinese matching questions
   - 5 fill-in-the-blank sentences
   - Answer key at the bottom

## Example Trigger

User says: "帮我整理第七章的术语" or "Study vocabulary for Chapter 7"
