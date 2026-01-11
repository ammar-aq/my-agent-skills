# PM Status Reporter

Transform messy team updates into professional Executive Status Reports following PMP standards in under 10 minutes.

## Overview

The pm-status-reporter skill automates the creation of executive-level project status reports by:
- Converting informal team updates into structured PMP-compliant reports
- Determining RAG status (Red/Amber/Green) based on project health
- Generating BLUF (Bottom Line Up Front) executive summaries
- Identifying and categorizing risks with mitigation strategies
- Extracting actionable next steps with clear ownership

Reduces weekly status report preparation time from 90 minutes to 10 minutes.

## Usage

### Quick Start

Simply paste your raw team updates and ask for a status report:

```
Generate status report from this:
[paste your chat logs, emails, or notes here]
```

### Alternative Invocations

```
Create executive status report from these updates: [content]
```

```
Turn this into a PMP status report: [content]
```

```
Generate weekly status report: [content]
```

## Input Formats

Accepts any informal format:
- Slack/Teams/Discord chat logs
- Email thread excerpts
- Bullet-point notes from standup meetings
- Mixed text from multiple sources
- Voice-to-text transcriptions

## Output Structure

The skill generates a professional report with:

1. **PROJECT HEALTH** - RAG status (Green/Amber/Red) with justification
2. **EXECUTIVE SUMMARY** - 2-sentence BLUF for leadership
3. **THIS WEEK'S PROGRESS** - Completed items and in-progress work
4. **RISKS AND BLOCKERS** - Categorized by severity with mitigation plans
5. **NEXT STEPS** - Action items with owners and key milestones
6. **DEPENDENCIES** - External blockers requiring attention

## RAG Status Definitions

**Green**: Project is on track
- No critical blockers
- Meeting timeline and budget
- Minor risks with mitigation in place

**Amber**: Project has warning signs
- Some blockers but manageable
- Minor timeline slippage possible
- Moderate risks requiring attention

**Red**: Project is at risk
- Critical blockers impacting delivery
- Significant timeline or budget impact
- High-severity risks without clear mitigation

## Examples

### Example 1: Simple Weekly Update

**Input**:
```
This week:
- deployed v2.3 to production
- fixed the login bug
- still waiting on legal approval for terms
- team is working on mobile app
- launch planned for next friday
```

**Output**: Professional status report with Green status, completed items listed, legal approval flagged as dependency.

### Example 2: Project with Blockers

**Input**:
```
updates: api done, frontend 80% complete, but our cloud provider had outage yesterday which set us back 2 days. client wants demo on monday but dont think well make it. also budget is running low, might need more $$
```

**Output**: Amber/Red status report highlighting cloud outage impact, timeline risk to Monday demo, and budget constraint requiring escalation.

### Example 3: Chat Log Format

**Input**:
```
[Copy-paste of Slack conversation with multiple team members discussing progress, blockers, and upcoming work]
```

**Output**: Synthesized executive report consolidating all team member inputs into structured format.

## Best Practices

1. **Include context** - Mention project name, launch dates, or key milestones if known
2. **Paste everything** - Don't filter; let the skill extract relevant information
3. **Weekly cadence** - Use every week for consistent executive communication
4. **Add dates** - Include timeframes for blockers and deadlines when possible
5. **Name owners** - Mention team member names for action item assignment

## Use Cases

- Weekly executive status reports
- Sprint retrospective summaries
- Incident post-mortems for leadership
- Monthly steering committee updates
- Board meeting project updates
- Stakeholder communication during critical phases

## PMP Standards Applied

The skill follows Project Management Professional (PMP) best practices:
- **BLUF Communication**: Bottom Line Up Front for executive audiences
- **RAG Status**: Red/Amber/Green health indicators
- **Risk Management**: Severity assessment and mitigation strategies
- **Stakeholder Communication**: Professional, jargon-free language
- **Action-Oriented**: Clear ownership and next steps

## Success Metrics

- Time saved: 90 minutes → 10 minutes per report
- Consistency: Standardized format across all project updates
- Clarity: Executive-friendly language avoiding technical jargon
- Completeness: All critical information captured and categorized

## Limitations

- Requires sufficient input detail to determine accurate RAG status
- Cannot infer information not present in the input
- Works best with recent updates (current week's activity)
- May need user clarification for ambiguous blocker severity

## Modifying the Skill

To customize the report format:

1. Edit `SKILL.md` Output Format section to adjust report structure
2. Modify RAG determination criteria in Step 3 of Procedure
3. Update BLUF summary style in Step 4 for your organization's preferences
4. Add company-specific sections (e.g., Budget Status, Resource Allocation)

## Tips

- Use for recurring weekly reports to establish consistent communication rhythm
- Combine with meeting notes tool for automated standup-to-status-report pipeline
- Archive generated reports for historical project tracking
- Share report template with stakeholders so they know what to expect
- Adjust RAG thresholds based on your organization's risk tolerance
