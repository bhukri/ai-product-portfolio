# Insurance FAQ Chatbot

An AI-powered chatbot built with Claude to answer common insurance questions 
for customers, brokers, and internal staff.

## What it does
- Answers questions on coverage types, claims process, and policy terms
- Stays in scope — redirects off-topic questions professionally
- Handles distressed users (post-accident, post-loss) with empathy first
- Refuses to quote prices or give legal advice (compliance guardrail)

## Tools used
- Claude.ai (Projects + system prompt)
- No code required

## Key product decisions
- Named persona ("Aria") to anchor tone consistency
- Hard guardrails on pricing and legal advice to manage regulatory risk
- Empathy trigger for distressed users — insurance conversations often 
  happen after difficult events
- 200-word response cap to keep answers scannable on mobile

## Test results
See test-results.md for output samples across 5 test scenarios.
