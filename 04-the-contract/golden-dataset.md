# Golden Dataset & Reliability Contract

## Golden Dataset Spec

| # | Input | Expected Output | Edge Case? | Judge Type |
|---|-------|----------------|-----------|-----------|
| 1 | | | Y/N | rule / LLM |
| 2 | | | Y/N | rule / LLM |
| 3 | | | Y/N | rule / LLM |
| 4 | | | Y/N | rule / LLM |
| 5 | | | Y/N | rule / LLM |

**Adversarial rows included:** __
**Coverage gaps identified by partner:**
Golden Dataset — Module 4

Test cases:
  1. Edge: Y · Judge: both — IN: System is checking merchant permissions/consent before using their shoppers details → OUT: Cx hits Pay through Agentic Commerce and systems first verifies for consent documents (permission already received to save card details check)
  2. Edge: Y · Judge: both — IN: Take shopper preferences before making recommendations → OUT: You liked this previous week/ You viewed this previous week recommendations
  3. Edge: Y · Judge: LLM — IN: Shows steps taken to process a transaction → OUT: Need to show/keep cx updated on whats happening

Dataset health
- Total: 3
- Edge cases: 3 (100.0%)
- Judge mix: 0% rule / 33% LLM / 67% both


## Confidence UX Design

**Approach:** Golden Dataset — Module 4  Test cases:   1. Edge: Y · Judge: both — IN: System is checking merchant permissions/consent before using their shoppers details → OUT: Cx hits Pay through Agentic Commerce and systems first verifies for consent documents (permission already received to save card details check)   2. Edge: Y · Judge: both — IN: Take shopper preferences before making recommendations → OUT: You liked this previous week/ You viewed this previous week recommendations   3. Edge: Y · Judge: LLM — IN: Shows steps taken to process a transaction → OUT: Need to show/keep cx updated on whats happening  Dataset health - Total: 3 - Edge cases: 3 (100.0%) - Judge mix: 0% rule / 33% LLM / 67% both

**Confident (>90%):** Full answer, SHow what you are doing why you are doing and also ask at the end if you want me to take a feedback and reset and recommend something new entirely

**Uncertain (50-90%):** _(not set)_

**Not confident (<50%):** _(not set)_

**User control surface:** 

- Users see AI reasoning / drivers
- Corrections feed back into the model / dataset
- Users adjust the confidence threshold _(not yet)_
- Users correct & override outputs _(not yet)_


## Reliability Contract

| Metric | Target | Measurement | Alert Threshold |
|--------|--------|-------------|-----------------|
| Accuracy | | | |
| Hallucination rate | | | |
| Latency (p95) | | | |
| Drift velocity | | | |

## HITL Architecture
<!-- When does a human step in? What's the escalation path? -->

## Red-Team Findings
*What failure mode did your partner find that you missed?*
