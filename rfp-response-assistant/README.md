#RFP Response Assistant

An AI powered two stage RFP analysis and response tool for insurance technology vendors responding to insurer procurement processes.

## What it does
Paste any insurance technology RFP and the assistant works in two stages:

Stage 1 analyses the RFP and produces:
- Plain English RFP summary
- Full list of explicit requirements
- Likely scoring criteria in priority order
- Landmines that could disqualify a response
- Gaps and ambiguities to clarify before responding
- Three strategic win themes
- Confidence rating on RFP completeness

Stage 2 generates a structured first draft response:
- Executive summary led by win themes
- About us with placeholders for company details
- Solution section addressing each requirement
- Technical approach written for non-technical evaluators
- Implementation plan with honest risk flagging
- Data security and compliance section
- Insurance domain expertise section
- Client reference placeholders
- Commercial proposal with placeholder pricing
- Closing argument tied to win themes

## Key product decisions
- Two stage flow — analysis always comes before writing
- System prompt is completely generic and reusable across any insurance technology RFP
- RFP specific details only enter at conversation time
- Implementation timelines assessed against integration complexity — never accepted at face value
- Compliance claims must be explicitly evidenced not implied
- Client references flagged as placeholders requiring human insertion before submission

## What I learned building this
The AI quietly absorbed details from my test RFP into the system prompt rules — making it specific to one RFP instead of reusable across all of them. 
I only caught it because of my consulting background. I rewrote the entire prompt from scratch to keep the system prompt generic and let RFP specific 
context come in at conversation time only.That one architectural decision is the difference between a prompt and a product.

## Important limitation
This tool produces a structured first draft. Domain specific details including regulatory references, integration versioning, and compliance documentation 
standards should always be reviewed by a qualified specialist before submission. This is a productivity tool not a replacement for expert judgment.

## Versions
system-prompt-v1.md — first version, contained RFP specific rules baked into the instructions
system-prompt-v2.md — rewritten generic version, works on any insurance technology RFP

## Test output
test-stage1-northbridge.md — full Stage 1 analysis on a synthetic Northbridge Insurance AI claims triage RFP

## Tools used
- Claude.ai Projects
- No code required

## ML concept learned
Retrieval-Augmented Generation (RAG) — keeping the system prompt as the stable knowledge layer and letting the user supplied document provide the 
dynamic context at query time. This is the same architectural principle that makes enterprise AI products stay current without retraining.
