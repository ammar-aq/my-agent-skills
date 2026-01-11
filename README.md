# My Agent Factory - AI-300 Checkpoint A1

**Name:** Ammar Kazi

**ID:** @ammarkazi-aq-cikv

Loom link: https://www.loom.com/share/8d4ed49242224d1e81cf6ac458046046
---

## Overview

This is my Agent Factory - a collection of 4 reusable Claude Code skills that automate repetitive tasks from both my student and professional work. These skills follow the Agent Factory pattern with a project constitution (CLAUDE.md) and a meta-skill (skills-builder) that manufactures other skills automatically.

**Total Time Saved:** 6+ hours per week

---

## The Skills

### 1. Assignment Understander
**Type:** Student Tool  
**What it replaces:** Spending 30-60 minutes confused about assignment requirements

**What it does:**
- Takes confusing assignment text
- Breaks it down into clear sections:
  - Simple explanation
  - Core requirements checklist
  - Step-by-step action plan
  - Success criteria
  - Time estimates
  - Common mistakes to avoid

**Metrics:**
- Time saved: 45 minutes per assignment
- Frequency: 3-5 assignments per week
- Quality: Never miss requirements

**Usage:** Used on this very AI-300 assignment to understand what to build!

---

### 2. Skills Builder (Meta-Skill)
**Type:** Factory Tool  
**What it replaces:** Manually creating SKILL.md files and folder structures

**What it does:**
- Generates new skills automatically
- Supports both interactive and single-sentence modes
- Creates complete folder structure with SKILL.md and README.md
- Enforces CLAUDE.md constitution standards

**Metrics:**
- Time saved: 1-2 hours per new skill
- Frequency: Used to build skills #3 and #4
- Quality: Consistent format, zero errors

**Usage:** Used to build the research-paper-analyzer and pmp-status-reporter skills

---

### 3. Research Paper Analyzer
**Type:** Student Tool  
**What it replaces:** Reading 20-30 page research papers manually

**What it does:**
- Analyzes AI research papers (PDF or text)
- Extracts:
  - Core contribution
  - Methodology and architecture
  - Key results
  - Limitations
  - Critical analysis questions
- Creates structured markdown summary

**Metrics:**
- Time saved: 35 minutes per paper (45min → 10min)
- Frequency: 3-5 papers per week
- Quality: Catches key points that would be missed skimming
- **Total weekly savings:** ~2.5 hours

---

### 4. PMP Status Reporter
**Type:** Professional Tool  
**What it replaces:** Manual creation of executive status reports every Friday

**What it does:**
- Takes messy team updates (Slack messages, emails, chat logs)
- Transforms into professional PMP-standard status report with:
  - RAG (Red/Amber/Green) health indicator
  - Executive summary (BLUF style)
  - This week's progress
  - Risks and blockers with mitigation strategies
  - Next steps with owners

**Metrics:**
- Time saved: 80 minutes per week (90min → 10min)
- Frequency: Weekly (every Friday)
- Quality: Professional, consistent formatting
- **Total weekly savings:** 1.3 hours

---

## Project Architecture

### Constitution: CLAUDE.md
The project follows a strict constitution that defines:
- Skill format standards (YAML frontmatter required)
- Procedure and output format rules
- Tone and formatting guidelines
- Skill activation triggers

All skills automatically follow these rules.

### Meta-Pattern: Skills Builder
Skills #3 and #4 were manufactured using the skills-builder meta-skill, demonstrating the "Agent Factory" pattern where agents build other agents.

---

## Total Impact

| Metric | Value |
|--------|-------|
| **Skills Built** | 4 (1 meta-skill + 3 working skills) |
| **Time Saved Per Week** | 6+ hours |
| **Student Work Automated** | Assignment understanding, paper analysis |
| **Professional Work Automated** | Executive status reporting |
| **Actual Usage This Week** | Assignment Understander used on AI-300 project |

---

## How to Use

### Prerequisites
- Claude Code installed (`claude --version` to verify)
- Logged in to Claude account

### Running a Skill

1. Navigate to project root:
```bash
   cd ~/Documents/my-agent-skills
```

2. Start Claude Code:
```bash
   claude
```

3. Use natural language:
   - "I have a confusing assignment in assignment.txt"
   - "Analyze this research paper: paper.pdf"
   - "Create a status report from these updates: [paste text]"

Claude automatically detects which skill to use based on your input.

---

## Skills vs. Traditional Automation

**Why skills are better than scripts:**
- ✅ Natural language interface (no command-line flags)
- ✅ Context-aware activation
- ✅ Portable across Claude surfaces (Code, .ai, API)
- ✅ Self-documenting (SKILL.md explains everything)
- ✅ Easy to modify and extend

---

## Project Structure
```
my-agent-skills/
├── README.md                      (this file)
├── CLAUDE.md                      (project constitution)
├── assignment-understander/
│   ├── SKILL.md
│   └── README.md
├── skills-builder/
│   ├── SKILL.md
│   └── README.md
├── research-paper-analyzer/
│   ├── SKILL.md
│   └── README.md
└── pmp-status-reporter/
    ├── SKILL.md
    └── README.md
```

---

## Success Signal Achieved

**Assignment requirement:** "At least one skill replaces a manual task for you this week"

✅ **Achieved:** Used assignment-understander on the AI-300 assignment itself, saving 45 minutes of confusion and ensuring all requirements were captured.

---

## What I Learned

1. **Spec-Driven Development Works:** Writing SKILL.md before implementation ensures clarity
2. **Meta-Skills Are Powerful:** The skills-builder manufactured skills #3 and #4 in minutes
3. **Constitution Pattern:** CLAUDE.md ensures consistency across all skills
4. **Real Usage Matters:** Building for actual problems (not demos) creates lasting value
5. **Agent Factory Model:** Using agents to build agents scales capability exponentially

---

## Future Enhancements

- Add AI Concept Converter skill for studying complex math/ML concepts
- Add Code Commentator skill for lab assignments
- Integrate MCP servers for external data sources
- Deploy skills to team members for shared productivity gains

---

**Built with:** Claude Code v2.1.1  
**Framework:** Agent Skills standard (agentskills.io)  
**Course:** AI-300 - Building Digital FTEs  
**Institution:** Panaversity
