---
name: writing-documentation
description: Writes and updates project documentation following established formatting rules. Use when the user asks to write, generate, or update documentation.
---

# Writing Documentation

When writing or updating documentation for this project, you MUST strictly adhere to the following formatting and styling rules to maintain consistency with existing documentation:

1. **Emojis in Headings**: Every heading (H1, H2, H3) MUST start with a relevant emoji.
   - Example H1: `# 🚀 Deployment Guide`
   - Example H2: `## 📱 Part 1. Client Application`
   - Example H3: `### 🤖 1. Automatic Deployment`

2. **Numbered Subsections**: H3 (`###`) and lower-level headings should generally be numbered if they are part of a sequence or a list of items.
   - Example: `### 💡 2. The Solution: A Dedicated Generation API`

3. **Introduction**: Immediately below the main H1 title, include a brief introductory paragraph describing what the document covers.

4. **GitHub Alerts**: Use standard GitHub Markdown alerts for critical information, warnings, or notes instead of plain text callouts.
   - Example: 
     > [!IMPORTANT]
     > Use this for important rules or gotchas.

5. **Lists with Bold Labels**: When using bulleted lists, boldly label the core concept before explaining it.
   - Example: `- **The Problem**: On the "Books" screen...`

6. **Language**: All documentation should be written in clear, professional English.

7. **Structure**: Break down complex topics into clear, logical sections. Use horizontal rules (`---`) to visually separate major parts of the document.

8. **Concise & Objective Tone**: Remove unnecessary adjectives and emotional coloring. Technical documentation should strictly focus on "what" and "why". If there's a result, express it with concrete specifics and metrics rather than subjective descriptions (e.g., avoid words like "massive", "beautiful", or "dramatically"). Make the text as concise as possible without losing the core meaning.

Use these rules every time you generate or modify `.md` files in the `docs/` directory.
