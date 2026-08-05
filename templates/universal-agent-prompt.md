# Universal AI Service Demo Prompt

Use this with Codex, Claude Code, or another capable AI agent. Replace the bracketed fields before sending it.

```text
Help me build the smallest useful demonstration of this AI service.

SERVICE
[WHAT I WANT TO OFFER]

POSSIBLE BUYER
[WHO MAY HAVE THIS PROBLEM]

REPEATED PROBLEM
[WHAT IS SLOW, MESSY, OR INCONSISTENT TODAY]

USEFUL RESULT
[WHAT THE BUYER SHOULD BE ABLE TO SEE OR REVIEW]

INPUTS
Use only fictional data that you create for this demonstration. Include five cases:
1. one normal case;
2. one case with missing information;
3. one unclear or conflicting case;
4. one out-of-scope case;
5. one case that must be handed to a person.

LIMITS
- Do not connect to a real customer system or use private data.
- Do not send messages, publish content, make purchases, change permissions, or deploy externally.
- Do not invent policies, numbers, testimonials, savings, or customer results.
- Keep [IMPORTANT DECISION] human-controlled.
- Ask before any external-account action.

WORKFLOW
1. Restate the buyer, problem, useful result, and limits in plain English.
2. Propose the smallest version with one main job.
3. List the files, screens, or data needed.
4. Build or draft it in small steps.
5. Test all five fictional cases.
6. Explain failures and fix them.
7. Prepare a two-minute walkthrough and a list of honest limitations.

DONE WHEN
- all five fictional cases work or fail safely;
- the useful result is obvious to a non-technical buyer;
- important actions wait for human approval;
- no private data or secret is present;
- I can demonstrate the result in under two minutes;
- you give me the exact next question to ask a possible buyer.
```

## Review prompt

After the first result, send this:

```text
Review the demonstration as a skeptical small-business buyer.

Find:
- anything confusing or too technical;
- claims that are not supported;
- hidden assumptions;
- missing or unsafe edge cases;
- actions that need human approval;
- features that do not help the main result.

Then give me a shorter correction plan. Do not add features unless they solve a problem found in the review.
```

The agent can help build and review the demonstration. You remain responsible for claims, access, privacy, client communication, price, and delivery.
