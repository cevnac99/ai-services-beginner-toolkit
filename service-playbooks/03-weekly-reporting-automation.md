# Weekly Reporting Automation

## The simple offer

Help an agency, consultant, or small team turn approved numbers and notes into a consistent weekly update that a manager can review quickly.

## Who may buy it

Agencies, freelancers, operations teams, project managers, and consultants who manually assemble the same update every week.

## The repeated problem

Information lives in several files, the report format changes, and important blockers or decisions disappear inside long updates.

## Build this first

A fictional report generator that accepts approved inputs and produces:

- period and source checklist;
- key numbers exactly as provided;
- completed work;
- blockers and missing inputs;
- decisions needed;
- next actions with owners;
- verification status.

## Five fictional test cases

1. Complete weekly input with all required numbers.
2. Missing metric or reporting period.
3. Two sources that disagree.
4. Unapproved metric or irrelevant narrative.
5. Result that could be misread as a guarantee or causal claim.

## Copyable agent prompt

```text
Build a fictional weekly reporting demonstration for a [TEAM OR SERVICE].

Use only the numbers and notes supplied in each test case. Never calculate a missing value or claim that one event caused another unless the input explicitly proves it.

Return: reporting period, sources received, key numbers, completed work, blockers, missing inputs, decisions needed, next actions, and verification warnings.

Create five cases: complete, missing data, conflicting sources, out-of-scope input, and a case that needs human interpretation.

Done when every number is traceable, missing information is visible, and a manager can review the report in under two minutes.
```

## Questions for a possible buyer

- Who reads the report and what decision do they make from it?
- Which numbers must be copied exactly?
- Where do the approved inputs come from?
- What is usually missing or disputed?
- Which conclusions require a manager rather than an assistant?

## What you can deliver

A repeatable report template, input checklist, source-to-output map, five-case test report, and review instructions.

## Human-controlled boundary

People verify numbers, approve interpretations, explain causes, and decide what is shared externally.

## Next move

Rebuild one old report with fictional values and ask its usual reader what information they scan first.
