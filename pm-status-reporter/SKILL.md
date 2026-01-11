---
name: "pm-status-reporter"
description: "Transform messy team updates, chat logs, and informal notes into professional Executive Status Reports following PMP standards. Includes RAG status determination, BLUF summaries, and risk mitigation strategies. Reduces report preparation from 90 minutes to 10 minutes. Use when generating weekly status reports for leadership."
version: "1.0.0"
---

## When to Use

Activate this skill when the user:
- Needs to create a weekly project status report for executives or stakeholders
- Has raw team updates, chat logs, email threads, or bullet points to consolidate
- Asks to "generate status report" or "create executive summary"
- Provides informal project updates that need to be professionalized
- Requests RAG status assessment or project health evaluation

## Procedure

### Step 1: Ingest Raw Input

Accept input in any format:
- Copy-pasted chat logs (Slack, Teams, Discord)
- Email thread excerpts
- Bullet-point notes from team members
- Informal text descriptions
- Mix of multiple sources

Read all provided content thoroughly.

### Step 2: Analyze Project Health

Review the input to identify:
- **Progress indicators**: Completed tasks, milestones hit, deliverables shipped
- **Blockers**: Issues preventing forward movement
- **Risks**: Potential problems that could impact timeline or quality
- **Timeline impact**: Are deadlines at risk?
- **Resource constraints**: Team capacity, budget, or dependency issues

### Step 3: Determine RAG Status

Assign a project health color based on PMP standards:

**Green**: Project is on track
- No critical blockers
- Meeting timeline and budget
- Minor risks with mitigation plans in place

**Amber**: Project has warning signs
- Some blockers present but manageable
- Minor timeline slippage possible
- Moderate risks requiring attention

**Red**: Project is at risk
- Critical blockers impacting delivery
- Significant timeline or budget impact
- High-severity risks without clear mitigation

Provide one-line justification for the assigned status.

### Step 4: Synthesize BLUF Executive Summary

Create a 2-sentence summary for leadership using Bottom Line Up Front (BLUF) style:
- Sentence 1: Overall project status and key outcome
- Sentence 2: Most critical information (blocker, achievement, or risk)

Use clear, corporate language avoiding technical jargon.

### Step 5: Categorize Progress Items

Organize information into structured categories:

**Completed This Week**:
- List all finished deliverables, tasks, or milestones
- Use past tense and active voice
- Focus on business value, not technical details

**In Progress**:
- Current work streams and their status
- Expected completion dates if available

### Step 6: Identify Risks and Mitigation

Extract and structure risks:
- **Risk description**: What could go wrong
- **Severity**: Critical, High, Medium, Low
- **Mitigation strategy**: Specific action to reduce or eliminate risk
- **Owner**: Who is responsible (if mentioned in input)

### Step 7: Extract Action Items

Identify next week's priorities:
- Clear action items with owners (if specified)
- Dependencies that must be resolved
- Key milestones or deadlines approaching

### Step 8: Format Output

Structure the report according to the Output Format section below using professional PMP terminology.

## Output Format

```
# EXECUTIVE STATUS REPORT
**Date**: [Current Week Ending Date]
**Project**: [Project Name if provided, otherwise "Project Update"]

---

## PROJECT HEALTH: [🟢 GREEN | 🟡 AMBER | 🔴 RED]
**Justification**: [One-line reason for status]

---

## EXECUTIVE SUMMARY
[2-sentence BLUF summary for leadership. Sentence 1: Overall status and outcome. Sentence 2: Most critical information.]

---

## THIS WEEK'S PROGRESS
- [Completed item 1 - business value focused]
- [Completed item 2 - business value focused]
- [Completed item 3 - business value focused]

**In Progress**:
- [Active work stream 1]
- [Active work stream 2]

---

## RISKS AND BLOCKERS

### Critical
- **[Risk/Blocker Description]**
  - Severity: Critical
  - Impact: [Timeline, budget, or quality impact]
  - Mitigation: [Specific action plan]
  - Owner: [Name if available]

### High
- **[Risk/Blocker Description]**
  - Severity: High
  - Impact: [Impact description]
  - Mitigation: [Mitigation strategy]
  - Owner: [Name if available]

### Medium
[Only include if present in input]

---

## NEXT STEPS
- [ ] [Action item 1 with owner if specified]
- [ ] [Action item 2 with owner if specified]
- [ ] [Action item 3 with owner if specified]

**Key Milestones**:
- [Upcoming milestone 1 - Date]
- [Upcoming milestone 2 - Date]

---

## DEPENDENCIES
[List external dependencies blocking progress, if any. Omit section if none.]

---
```

## Example

**User Input**:
```
Generate status report from this:

hey team - quick updates:
- sarah finished the API integration finally!! took longer bc of auth issues
- mike is still stuck on database migration, keeps timing out
- design mockups approved by client yesterday
- launch date is oct 15 but honestly idk if we'll make it with the db problems
- need to schedule testing next week
- budget meeting got pushed to friday
- the vendor still hasn't sent us the contract, been 2 weeks now, starting to worry
```

**Claude Response**:
```
# EXECUTIVE STATUS REPORT
**Date**: Week Ending October 6, 2024
**Project**: Project Update

---

## PROJECT HEALTH: 🟡 AMBER
**Justification**: Database migration blocker and vendor contract delay pose timeline risk to October 15 launch.

---

## EXECUTIVE SUMMARY
Project has completed API integration and secured client approval on designs, but faces technical blockers in database migration. Vendor contract delay (2 weeks overdue) and database timeout issues require immediate escalation to maintain October 15 launch date.

---

## THIS WEEK'S PROGRESS
- Completed API integration with authentication layer implementation
- Secured client approval on design mockups
- Scheduled budget alignment meeting for Friday

**In Progress**:
- Database migration experiencing timeout issues (blocked)
- Vendor contract review (pending vendor response)

---

## RISKS AND BLOCKERS

### Critical
- **Database Migration Timeouts**
  - Severity: Critical
  - Impact: Blocking development progress; direct threat to October 15 launch date
  - Mitigation: Escalate to database team for immediate troubleshooting; consider parallel migration approach or infrastructure scaling
  - Owner: Mike

### High
- **Vendor Contract Delay (2 Weeks Overdue)**
  - Severity: High
  - Impact: Legal and procurement risk; potential launch blocker if contract affects deliverables
  - Mitigation: Executive escalation to vendor leadership; identify backup vendor if no response within 48 hours
  - Owner: [Unspecified - assign owner]

---

## NEXT STEPS
- [ ] Resolve database migration timeout issue (Mike)
- [ ] Schedule testing sessions for next week (Team)
- [ ] Escalate vendor contract delay to executive sponsor
- [ ] Conduct budget meeting on Friday
- [ ] Assess October 15 launch feasibility based on database resolution timeline

**Key Milestones**:
- Budget Meeting - Friday, October 6
- Planned Launch Date - October 15 (at risk)

---

## DEPENDENCIES
- Database team support required for migration timeout resolution
- Vendor contract approval required before launch
- Testing environment availability needed for next week

---
```
