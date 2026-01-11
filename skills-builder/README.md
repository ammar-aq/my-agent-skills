# Skills Builder

A meta-skill that generates new Claude Code skill folders automatically, following the project constitution defined in CLAUDE.md.

## Overview

The skills-builder skill automates the creation of new skills by:
- Generating properly formatted SKILL.md files
- Creating README.md documentation
- Adding example files when applicable
- Enforcing naming conventions and structure

## Usage

### Quick Start (Single-Sentence Mode)

Simply describe what you want in one sentence:

```
Build me a PDF summarizer
```

```
Create a skill that converts CSV to JSON with validation
```

The skill will automatically:
- Extract the skill name
- Identify inputs and outputs
- Generate all required files
- Provide next steps

### Interactive Mode

For more control, ask to build a skill without details:

```
Build a new skill
```

Claude will guide you through:
1. Skill naming
2. Problem definition
3. Input specification
4. Output specification
5. Special requirements

## What Gets Generated

Every skill folder includes:

1. **SKILL.md** - The instruction file Claude reads
   - Frontmatter with metadata
   - When to Use section
   - Step-by-step Procedure
   - Output Format specification
   - Concrete Examples

2. **README.md** - User documentation
   - Overview and purpose
   - Usage instructions
   - Examples

3. **Supporting files** (when applicable)
   - example-input.txt
   - Templates
   - Configuration files

## Folder Structure

```
my-agent-skills/
├── CLAUDE.md (project constitution)
├── skills-builder/
│   ├── SKILL.md
│   └── README.md
└── [your-new-skill]/
    ├── SKILL.md
    ├── README.md
    └── [supporting files]
```

## Standards Enforced

All generated skills follow:
- YAML frontmatter format
- Consistent section structure
- Professional tone (no emojis)
- Clear trigger conditions
- Step-by-step procedures
- Concrete examples

## Examples

### Example 1: Data Processing Skill

**Input**: "Build me a log file analyzer"

**Output**:
- Creates `../log-analyzer/` folder
- Generates SKILL.md with log parsing procedures
- Creates example-log.txt
- Provides usage instructions

### Example 2: Content Transformation

**Input**: "Create a skill that converts API responses to documentation"

**Output**:
- Creates `../api-to-docs/` folder
- Generates SKILL.md with transformation steps
- Creates example-response.json
- Includes formatting guidelines

## Modifying Generated Skills

After generation:
1. Review SKILL.md for accuracy
2. Adjust procedure steps if needed
3. Add more examples
4. Update trigger conditions
5. Test with real inputs

## Best Practices

- Use kebab-case for skill names
- Keep descriptions concise and action-oriented
- Include concrete examples
- Define clear input/output formats
- Specify trigger conditions explicitly

## Troubleshooting

**Skill not activating?**
- Check "When to Use" section matches your input
- Verify skill is in Claude Code skills directory

**Wrong output format?**
- Review "Output Format" section in SKILL.md
- Add more specific formatting rules

**Need to update a skill?**
- Edit SKILL.md directly
- Test changes with sample input
- Update version number if significant changes
