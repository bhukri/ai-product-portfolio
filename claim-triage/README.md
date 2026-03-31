# Claim Triage Tool
An AI powered claim triage tool that classifies incoming claim descriptions instantly.

## What it does
- Classifies claim type, urgency, red flags and complexity
- Scoped to the claimant's perspective only
- Flags when more information is needed

## Key product decisions
- Urgency reflects current situation, not past events
- Recommended actions scoped to claims handler role only
- Complexity scale defined from domain knowledge
- Third party details only relevant if they affect the claimant's claim journey

## Note
This is a learning prototype. In production this tool would be scoped to a specific line of insurance with policy context pre-loaded for each claimant.

## Tools used
- Claude.ai Projects
- No code required

## ML concept learned
Classification models assign inputs to categories. The model is only as good as the rules you give it.
