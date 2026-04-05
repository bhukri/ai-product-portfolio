# StyleAI — AI Outfit Decider
## Product Requirements Document v1.0

---

## Problem statement
Getting dressed in the morning is a daily decision that drains mental energy before the day has even started. The problem is not a lack of clothes. It is having 
too many choices, too little time, and no confident starting point. Most people own more than they wear because they cannot visualise combinations quickly under 
time pressure.

---

## Target user
Primary: Professional women with a full wardrobe who experience decision fatigue getting dressed for work or social occasions, particularly in the morning.

User quote from discovery:
"Just too many clothes and getting overwhelmed. In the AM when in a rush."

---

## User needs (from discovery interview)
1. Scan the whole closet in one photo — not item by item
2. Get one confident outfit suggestion, not endless options
3. Small variations on the core outfit, plus one totally different alternative on request
4. Know why the outfit works — weather, occasion, style
5. Calendar awareness — what am I doing today shapes what I should wear
6. End of day feedback loop — what worked, what did not, and why
7. Learn preferences over time — style, fit, formality

---

## ML capabilities required
| Capability | Purpose |
|---|---|
| Image understanding | Read closet photos and identify clothing items |
| Extraction | Pull individual items from a group wardrobe photo |
| Recommendation | Suggest outfit combinations from available items |
| Personalisation | Adapt suggestions based on feedback history |
| Calendar integration | Pull today's schedule to inform outfit context |
| Preference learning | Remember what worked and what did not over time |

---

## Product versions

### v1 — Prototype (building today)
What we are building now with available tools.

Features included:
- Single closet group photo upload
- User confirms basics via quick button selection
- Occasion and weather input via buttons
- One outfit recommendation with two small variations
- One totally different alternative on request
- Brief explanation of why it works
- End of day feedback button — worked or did not work

Features not included in v1:
- Calendar integration
- Persistent memory across sessions
- Preference learning over time
- Style trend awareness

### v2 — Connected product (roadmap)
- Google Calendar or Outlook integration — StyleAI knows your day without you typing it
- Persistent user profile — remembers your wardrobe, your preferences, and your feedback history
- End of day feedback loop stored and used to refine future suggestions
- Seasonal wardrobe awareness — surfaces items you have not worn recently

### v3 — Intelligent stylist (future vision)
- Learns personal style signature over time
- Flags items that repeatedly do not work and suggests retiring them
- Suggests one new piece per month that would fill a genuine gap in the wardrobe based on usage patterns
- Integrates weather API for real time conditions

---

## Success metrics for v1
- User gets an outfit suggestion in under 2 minutes
- Suggestion uses only items visible in the photo
- User rates the suggestion as useful or not useful
- Zero suggestions of items not in the wardrobe

---

## Absolute nos (from user discovery)
- Never suggest buying something unless explicitly asked
- Never give more than one core outfit unprompted
- Never make negative comments about fit or style choices
- Never require the user to photograph every item individually
- Never suggest an outfit that does not match the stated occasion — no casual suggestions for formal events and vice versa
- Never ignore the weather context — never suggest a sleeveless top on a cold day
- Never repeat the same outfit suggestion in the same session
- Never suggest an item that is not clearly visible in the uploaded photo
- Never ask more than two clarifying questions — if context is missing make a reasonable assumption and state it
- Never overwhelm with explanations — keep reasoning brief and practical

---

## Key product decisions and rationale

**Group photo over individual items**
User does not have time to photograph 50 pieces. One closet shot with a basics assumption is the right starting point for v1. Accuracy improves in v2 with 
persistent wardrobe memory.

**One outfit with variations over multiple options**
Discovery showed the user wants a confident starting point, not a menu. Decision fatigue is the problem — more options make it worse, not better.

**End of day feedback in v1**
Even without persistent memory, capturing feedback creates the habit loop that v2 will build on. It also gives the product team real data on what is working.

**Calendar integration deferred to v2**
Requires API access and authentication — out of scope for a no-code prototype. Documented on roadmap so it is not forgotten.

---

## Discovery process
This spec was built from a user discovery interview conducted with the primary user before any building began. Five questions were asked covering the core 
problem, timing of pain, expected output format, explanation preferences, and absolute constraints.

This is the right order. Understand the problem before building the solution.

---

## Tools for v1 prototype
- Typebot — conversation flow and photo upload
- Claude API — image understanding and outfit generation
- No code required

## Status
Product spec: Done
v1 Prototype: In progress
