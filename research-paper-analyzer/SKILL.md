---
name: "research-paper-analyzer"
description: "Analyze complex AI research papers into structured summaries optimized for Masters-level study. Extracts core contributions, methodology, results, and generates critical thinking questions. Reduces reading time from 45 minutes to 10 minutes. Use when user needs to efficiently understand academic AI papers."
version: "1.1.0"
---

## When to Use

Activate this skill when the user:
- Provides a research paper file (PDF or text) for analysis
- Asks to "analyze this paper" or "summarize this research"
- Requests extraction of key findings, methodology, or results from academic papers
- Needs to understand citations, references, or related work
- Wants structured output from academic literature

## Procedure

### Step 1: Identify Paper Source

Determine input type:
- PDF file path provided
- Text content pasted directly
- URL to paper (if accessible)

Read the paper content using appropriate tool (Read for PDFs/text files).

### Step 2: Extract Core Components

Parse and identify these standard academic paper sections:
1. **Title and Authors** - Full title, author names, affiliations
2. **Abstract** - Complete abstract text
3. **Introduction** - Research problem and motivation
4. **Methodology** - Approach, techniques, experimental design
5. **Results** - Key findings, data, figures mentioned
6. **Discussion** - Interpretation and implications
7. **Conclusion** - Summary of contributions
8. **References** - Citation count and key cited works

### Step 3: Analyze Content

For each section identified:
- Extract main points (3-5 bullet points per section)
- Identify key terms, concepts, and metrics
- Note any novel contributions or unique approaches
- Highlight limitations mentioned by authors

### Step 4: Synthesize Findings

Create high-level synthesis:
- Research question being addressed
- Main hypothesis or claim
- Primary contribution to the field
- Practical applications or implications
- Future work suggested

### Step 5: Generate Critical Analysis Questions

Develop 3 critical questions that:
- Challenge assumptions or design choices
- Probe deeper into methodology or results
- Connect to broader AI research context
- Encourage comparative analysis with other approaches
- Identify gaps or unexplored directions

Questions should promote Masters-level critical thinking and deeper comprehension.

### Step 6: Format Output

Structure analysis according to Output Format section below.

## Output Format

```
# Research Paper Analysis: [Paper Title]

## Metadata
- **Authors**: [Names and affiliations]
- **Publication**: [Journal/Conference, Year]
- **Citation Count**: [If available]

## Abstract Summary
[2-3 sentence distillation of abstract]

## Research Question
[What problem does this paper address?]

## Core Contribution
[Single paragraph describing the primary novel contribution to the field]

## Methodology & Architecture
- Approach: [Brief description]
- Architecture: [Model structure or system design if applicable]
- Techniques: [Key methods used]
- Data: [Dataset or experimental setup]

## Key Results
1. [Result 1 with metrics]
2. [Result 2 with metrics]
3. [Result 3 with metrics]
[Add more as needed]

## Limitations
- [Limitation 1 if mentioned]
- [Limitation 2 if mentioned]

## Critical Analysis Questions
1. [Question probing assumptions or methodology]
2. [Question connecting to broader AI context]
3. [Question identifying gaps or alternatives]

## Important Citations
- [Key reference 1]
- [Key reference 2]
- [Key reference 3]

## Quick Summary
[3-4 sentence summary suitable for quick reference]
```

## Example

**User Input**:
```
Analyze this research paper: /path/to/attention-is-all-you-need.pdf
```

**Claude Response**:
```
# Research Paper Analysis: Attention Is All You Need

## Metadata
- **Authors**: Vaswani et al. (Google Brain, Google Research)
- **Publication**: NeurIPS 2017
- **Citation Count**: 90,000+

## Abstract Summary
This paper introduces the Transformer architecture, a novel neural network model based entirely on attention mechanisms, eliminating recurrence and convolutions entirely while achieving superior performance on translation tasks.

## Research Question
Can a neural architecture based solely on attention mechanisms match or exceed the performance of recurrent and convolutional models for sequence transduction tasks?

## Core Contribution
The Transformer architecture is the first sequence transduction model to rely entirely on self-attention mechanisms without any recurrence or convolutions. This design enables highly parallelizable training while achieving state-of-the-art translation quality, fundamentally changing how sequence modeling is approached in deep learning.

## Methodology & Architecture
- Approach: Self-attention mechanism (scaled dot-product attention)
- Architecture: Encoder-decoder structure with stacked self-attention and feed-forward layers
- Techniques: Multi-head attention, positional encoding, residual connections, layer normalization
- Data: WMT 2014 English-German (4.5M sentence pairs) and English-French (36M sentence pairs) translation datasets

## Key Results
1. Achieves 28.4 BLEU on English-to-German translation, improving over existing best results by over 2 BLEU
2. Reaches 41.8 BLEU on English-to-French translation, establishing new state-of-the-art
3. Training is 10x faster than recurrent models, completing in 3.5 days on 8 GPUs
4. Generalizes to English constituency parsing with competitive F1 scores

## Limitations
- Requires explicit positional encodings since model has no inherent notion of sequence order
- Quadratic computational complexity O(n²) for very long sequences
- Limited evaluation on tasks beyond translation and parsing

## Critical Analysis Questions
1. How does the quadratic complexity of self-attention limit the Transformer's applicability to very long sequences (e.g., documents, long-form video), and what architectural modifications could address this?
2. Why do learned positional embeddings perform similarly to sinusoidal encodings, and what does this suggest about how the model represents sequential information?
3. Could the attention mechanism's ability to capture long-range dependencies be systematically compared against LSTMs with different forget gate configurations to isolate the architectural advantage?

## Important Citations
- Bahdanau et al. (2014) - Neural Machine Translation by Jointly Learning to Align and Translate
- Sutskever et al. (2014) - Sequence to Sequence Learning with Neural Networks
- Gehring et al. (2017) - Convolutional Sequence to Sequence Learning

## Quick Summary
The Transformer architecture replaces recurrence with self-attention mechanisms, achieving state-of-the-art translation quality (28.4 BLEU on EN-DE) while being 10x more parallelizable than LSTMs. This foundational work enabled the development of modern large language models like BERT and GPT by demonstrating that attention alone is sufficient for sequence modeling.
```
