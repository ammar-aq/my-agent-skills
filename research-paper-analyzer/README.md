# Research Paper Analyzer

Automatically analyze academic research papers and extract key information into structured summaries.

## Overview

The research-paper-analyzer skill processes academic papers (PDF or text format) and generates comprehensive analyses including:
- Abstract summaries
- Research questions and hypotheses
- Methodology descriptions
- Key findings and contributions
- Limitations and future work
- Important citations

## Usage

### Basic Analysis

Simply provide a path to a research paper:

```
Analyze this research paper: /path/to/paper.pdf
```

### Alternative Invocations

```
Summarize this research paper: paper.pdf
```

```
What are the key findings in this paper? [paste paper text]
```

```
Extract methodology from this research: /documents/study.pdf
```

## Input Formats

Supported input types:
- PDF files (`.pdf`)
- Text files (`.txt`, `.md`)
- Direct text paste of paper content
- URLs to accessible papers

## Output Structure

The skill generates a comprehensive analysis with:

1. **Metadata** - Authors, publication info, citations
2. **Abstract Summary** - Condensed abstract
3. **Research Question** - Core problem addressed
4. **Methodology** - Approach and techniques
5. **Key Findings** - Main results (numbered list)
6. **Main Contributions** - Novel additions to field
7. **Limitations** - Acknowledged weaknesses
8. **Implications** - Practical/theoretical significance
9. **Future Work** - Suggested research directions
10. **Important Citations** - Key referenced works
11. **Quick Summary** - 3-4 sentence overview

## Examples

### Example 1: Machine Learning Paper

**Input**:
```
Analyze /papers/deep-learning-nature-2015.pdf
```

**Output**: Structured analysis with methodology (deep neural networks), key findings (ImageNet performance), and contributions (representation learning advancement).

### Example 2: Medical Research

**Input**:
```
Summarize this clinical trial paper: /research/drug-efficacy-study.pdf
```

**Output**: Analysis focusing on experimental design, patient cohorts, efficacy results, and clinical implications.

### Example 3: Quick Reference

**Input**:
```
Give me a quick summary of this paper: /papers/quantum-computing.pdf
```

**Output**: Full analysis generated with emphasis on the "Quick Summary" section for rapid comprehension.

## Best Practices

1. **Provide complete papers** - Full papers yield better analysis than abstracts alone
2. **Check PDF quality** - Ensure PDFs are text-readable (not scanned images)
3. **Specify focus areas** - Request specific sections if needed ("focus on methodology")
4. **Use for literature review** - Analyze multiple papers to compare approaches
5. **Extract citations** - Identify important related work for further reading

## Use Cases

- Literature review for research projects
- Quick comprehension of unfamiliar papers
- Extracting methodology for replication studies
- Identifying key citations and references
- Preparing paper summaries for presentations
- Understanding contributions across multiple papers

## Limitations

- Works best with standard academic paper structure (IMRaD format)
- PDF quality affects extraction accuracy
- Cannot access papers behind paywalls without file access
- Analysis depth depends on paper clarity and organization

## Modifying the Skill

To customize the analysis:

1. Edit `SKILL.md` Procedure section to add/remove extraction steps
2. Modify Output Format to include additional sections
3. Update "When to Use" triggers for automatic activation
4. Add domain-specific terminology extraction

## Tips

- For multiple papers, analyze each separately then request comparative summary
- Request focus on specific sections: "analyze just the methodology"
- Ask follow-up questions: "What datasets were used?" after initial analysis
- Use for paper screening: Quick Summary helps decide if full read is needed
