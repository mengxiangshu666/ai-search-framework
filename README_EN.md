# AI Search Framework v2.11
> Stop letting AI give you confident nonsense. Start using a system.

---

## 🔥 Does this sound familiar?

- You asked AI a question, it answered smoothly with full confidence — and it was completely wrong
- AI cited "2024 data" that turned out to be from its training set, months out of date
- You asked the same question three times and got three different answers
- AI treated a marketing article as hard evidence, and you didn't catch it

**The problem isn't that AI is stupid. The problem is that AI has no system for thinking before it speaks.**

---

## What This Framework Is

The AI Search Framework is a **structured self-verification system for AI responses**. It's not about prompting better — it's about forcing AI to run a complete self-audit before answering you.

The core problem it solves: **the gap between AI's confidence and actual facts.**

---

## Who This Is For

- Anyone who uses AI for research or decision-making
- People relying on AI for investment, legal, or career advice
- AI application developers who need more reliable outputs
- Anyone tired of being misled by AI hallucinations

---

## Core Mechanism (Three Sentences)

**1. Mode Tiers** — The more serious the question, the stricter the AI's self-review. Simple facts use Quick mode; life-altering decisions use Deep mode.

**2. Four-Level Confidence Grid** — Every conclusion must be labeled: High / Medium / Low / Extremely Low. AI is not allowed to say "probably" without a clear label.

**3. Falsification Search** — AI must search for "why this could be wrong" — not just "why this is right." Can't find counter-evidence? Downgrade your confidence.

---

## Quick Start

**Three modes, remember them by use case:**

| Mode | When to Use | AI Search Rounds |
|---|---|---|
| **Quick** | Low-risk facts, casual queries | 1 round |
| **Standard** | Decisions, risk assessment, "is X good?" | 2 rounds (incl. falsification) |
| **Deep** | Investment, legal, major life direction, conflicting goals | 4+ rounds |

**One attitude to internalize:**
> AI answers too fast, too smooth, too confidently = danger signal

---

## Output Format (In Order)

AI responses must follow this structure:

**Step 1: Direct Answer** (1-5 sentences, conclusion first)
↓
**Step 2: Core Findings** (100-300 words each, with source labels)
↓
**Step 3: Next Steps** (30-80 words each, actionable)

**Forbidden order:**
- ❌ Background first → Conclusion buried last
- ❌ "This is a complex issue..." → then nothing
- ❌ Meta-analysis + self-evaluation + summary (AI wanking in circles)

---

## Strict Four-Level Confidence

| Level | Meaning | Use Case |
|---|---|---|
| **High** | Solid enough for action | Major decisions |
| **Medium** | Direction is right, verify further | General guidance |
| **Low** | Use with caution only | Initial research |
| **Extremely Low** | Stop. Go search more. | Critical information gap |

**Automatic downgrade triggers:**
- Only 1 independent source found
- Cannot find any counter-evidence
- Core info hasn't been updated in over 1 year (except historical)
- Fast-changing topic (AI tools/policy/prices) not updated in 1 week
- 2+ contradicting sources
- Marketing content treated as fact
- Any of the 13 taboos triggered

---

## Search Rules (Execute Each One)

1. **Source count:** Quick>=1 / Standard>=2 / Deep>=4 (independent = different org/author/domain)
2. **Counter-evidence:** Required for judgments/predictions/decisions. 3 rounds of rewording and still nothing → downgrade confidence
3. **Falsification search:** Search "why this might be wrong" — not "whether this is right"
4. **Honesty labels:** Every finding must be tagged `[Verified]` / `[Impression]` / `[Unknown]`. Any specific number needs a URL and date.
5. **Marketing detection:** Only positives / purchase links / sensational headlines → auto downgrade 1 level
6. **Freshness for fast-moving topics:** AI tools, policy, prices, stocks — older than 1 week is stale, add "this week" / "latest"
7. **Three date types:** Event date | Publication date | Index date (they can all be different)

---

## 13 Taboos (Trigger = Downgrade 1 Level)

1. Forcing a conclusion with insufficient info → Extremely Low
2. Hiding sources and uncertainty points
3. Only showing supporting evidence (counter-evidence is mandatory)
4. Self-bias-check written as a formality, doesn't change the conclusion
5. Vague freshness labels
6. Actionable next steps that aren't actually actionable
7. Fitting evidence to a predetermined answer
8. Using combined confidence labels (can't say "medium-high")
9. Outputting meta-analysis / self-evaluation / summary (AI showing off)
10. Long questions (>=200 words) analyzed without first organizing the information
11. Skipping the counter-evidence search when rewording
12. Passing [Impression] off as [Verified]
13. Specific numbers cited without a search source

---

## Handling Conflicting Goals

When >=2 goals contradict each other:

1. List all goals (>=3)
2. Score each goal (High/Medium/Low)
3. Mark each goal's irreversibility
4. Output a trade-off matrix
5. **Be explicit: there is no perfect option**

---

## Execution Rules

1. Execute search rules one by one. If a checkpoint fails, search again
2. Output order: Direct Answer → Core Findings → Next Steps
3. Core findings: Standard 100-200 words/item, Deep 150-300 words/item
4. Next steps: 30-80 words/item, must be actionable
5. Long questions (>=200 words) → first build an information extraction list, then analyze
6. Every number must be traceable to its source

---

## Freshness Guide

| Type | Priority |
|---|---|
| Predictions | Latest > Recent > Historical |
| Decisions | Latest > Historical trends |
| Facts | Historical accuracy |
| Historical | Primary sources > Secondary |
| Evaluations | Within last 1-3 months |
| Methods/Capabilities | Within last 3 years |

---

## Version Notes

- v2.10: Format reorganization, AI reading optimization, content unchanged
- v2.11: (current version)

**Design philosophy:** The quality of AI search isn't determined by the AI — it's determined by the framework you give the AI. This framework distills expert-level methodology on "how to judge if an AI answer is trustworthy" into a structured, executable process.
