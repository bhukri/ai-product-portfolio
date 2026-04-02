# Broker Onboarding Bot — Alex

A conversational AI onboarding specialist for a Canadian P&C insurance company. Alex onboards new brokers and helps existing brokers add new product lines.

## What Alex does
- Identifies whether the user is a new or existing broker
- Collects broker profile information one question at a time
- Explains appointment process, product appetite, commission structure, and claims referral process
- Presents numbered options throughout to simulate a button driven experience
- Handles out of scope questions with graceful referrals
- Closes with a full summary and clear next steps

## Conversation flows
- Flow A — New broker full onboarding journey
- Flow B — Existing broker adding a new product line

## Key product decisions
- One question at a time — never overwhelming the user
- Numbered options for all choice based questions
- Commission rates framed as guide only — never guaranteed
- Coverage and claims decisions always referred to specialists
- Warm but efficient tone — Alex feels like a colleague not a form
- Cross-border and specialist questions deflected gracefully to the right team

## Edge cases tested
- Out of scope question mid flow — cross-border commissions
- Multiple line selection — handled naturally
- Returning broker recognition — correct flow triggered instantly

## Upcoming upgrade
- Typebot integration with real clickable buttons and proactive greeting — planned for weekend power day

## Tools used
- Claude.ai Projects
- No code required

## ML concept learned
Conversational AI and dialogue management — keeping track of conversation state, user type, and flow position 
across a multi-turn interaction without losing context.
