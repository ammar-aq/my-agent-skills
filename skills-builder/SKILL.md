---
name: "skills-builder"
description: "Generate new Claude Code skill folders from interactive prompts or single-sentence requests. Creates SKILL.md, README.md, and optional example files following project constitution. Use when user asks to create, build, or generate a new skill."
version: "1.0.0"
---

## When to Use

Activate this skill when the user:
- Asks to "build a new skill"
- Requests "create a skill for [task]"
- Provides a single-sentence skill idea like "Build me a [tool]"
- Wants to generate a new reusable automation

## Procedure

### Step 1: Detect Mode

Analyze user input to determine mode:

**MODE A (Interactive)**: User asks to build a skill without full details
- Example: "Build a new skill"
- Example: "Create a skill"

**MODE B (Single-sentence)**: User provides complete context in one sentence
- Example: "Build me a PDF summarizer"
- Example: "Create a skill that converts CSV to JSON"

### Step 2: Gather Information

**For MODE A**: Ask these questions sequentially:
1. What should the skill be named? (use kebab-case)
2. What problem does this skill solve?
3. What are the expected inputs?
4. What are the expected outputs?
5. Are there any special requirements or constraints?

**For MODE B**: Extract from user input:
- Skill name (derive from task description)
- Problem statement
- Input/output types
- Key features

### Step 3: Generate Skill Folder

Create the following structure in `../[skill-name]/`:

1. **SKILL.md** - Main instruction file with:
   - Frontmatter (name, description, version)
   - ## When to Use
   - ## Procedure
   - ## Output Format
   - ## Example

2. **README.md** - User-facing documentation with:
   - Skill overview
   - Installation/setup (if needed)
   - Usage examples
   - Expected inputs/outputs

3. **example-input.txt** (optional) - Sample input file if the skill processes text files

### Step 4: Validate Output

Ensure generated SKILL.md:
- Has valid YAML frontmatter
- Description follows pattern: "[action verb] + [input type] + into/for + [output type] + [key features]. Use when [trigger conditions]."
- Contains all required sections
- Uses professional tone (no emojis)
- Includes concrete examples

### Step 5: Provide Next Steps

Inform user:
- Skill location: `../[skill-name]/`
- Files created
- How to test the skill
- How to modify or extend it

## Output Format

After skill generation, output:

```
Created new skill: [skill-name]

Location: /path/to/[skill-name]/

Files generated:
- SKILL.md (main instruction file)
- README.md (user documentation)
- [other files if applicable]

Next steps:
1. Review SKILL.md to ensure it matches your requirements
2. Test the skill by invoking it with sample input
3. Modify procedure or output format if needed
4. Add the skill to your Claude Code skills directory
```

## Example

**User Input (MODE B)**:
```
Build me a skill that converts markdown files to clean PDF documents with custom styling
```

**Claude Response**:
```
I'll create a markdown-to-pdf skill for you.

Analyzing request:
- Skill name: markdown-to-pdf
- Input: Markdown files
- Output: Styled PDF documents
- Key feature: Custom styling support

Creating skill folder at ../markdown-to-pdf/...
```

Then Claude generates:
- `../markdown-to-pdf/SKILL.md`
- `../markdown-to-pdf/README.md`
- `../markdown-to-pdf/example-input.md`

**User Input (MODE A)**:
```
Build a new skill
```

**Claude Response**:
```
I'll help you build a new skill. Let me gather some information:

1. What should the skill be named? (use kebab-case like "data-analyzer")
```

Then Claude proceeds through questions 2-5 before generating the skill folder.
