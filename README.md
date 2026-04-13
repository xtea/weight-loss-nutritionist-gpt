# Weight Loss Nutritionist GPT

An AI-powered weight loss **companion** — part coach, part food-logging sidekick, part 24/7 accountability friend. Built on an evidence-based nutrition foundation and engineered around what actually drives sustained weight loss: reducing the daily cognitive cost of applying what you already know.

**[Try it free on ChatGPT](https://chatgpt.com/g/g-69d902da41448191b094b5dc57ec331b-weight-loss-nutritionist)**

## Why This Design

Most diet GPTs are glorified calorie calculators. This one is different because it is engineered against the real failure mode of weight loss: **execution, not information**.

Analysis of 30+ Reddit posts from r/loseit, r/ChatGPT, r/CICO and others — summarized in [How Real People Use ChatGPT to Lose Weight](https://nanorhino.com/blog/how-real-people-use-chatgpt-to-lose-weight-reddit-research) — shows people succeed when AI does three specific things:

1. **Reduces tracking friction** — natural-language food logging instead of database lookups
2. **Offloads daily decisions** — meal plans, restaurant picks, "what can I make with this" questions
3. **Non-judgmental accountability** — 24/7 partner for the honest messages people can't send a human trainer

This GPT is built around all three, with explicit guardrails for the known failure modes of general-purpose chatbots (bad calorie estimates, no memory, math errors, passive cheerleading).

## Core Capabilities

- **Food Logging Mode** — describe a meal or paste a photo, get a structured log with confidence tags and liquid-calorie / hidden-oil flags. No database lookup, no barcode scanning.
- **State Snapshot Ritual** — a copy-pastable profile block the GPT generates on request so you can start fresh chats without losing your context (works around ChatGPT's memory limit).
- **Calorie Honesty Rule** — every estimate ships with a confidence range (±15-30%) and guidance on when to reach for a kitchen scale. No false precision.
- **Arithmetic Transparency** — BMR / TDEE / deficit calculations show their work inline so you can spot-check.
- **Safety Screening** — on first interaction, gently checks for medical conditions, underweight targets, psychiatric medications, teen/pregnancy status, and routes to the right playbook.
- **When to Challenge** — deliberately does not default to validation. Names repeat patterns, refuses unsafe deficits, calls out non-scale wins the user is missing.
- **HALT framework** — Kaiser Permanente's emotional-eating self-check (Hungry / Angry / Lonely / Tired) for pre-eating moments.
- **ADD / REDUCE / REPLACE** — never prescribes restriction. Suggests what to add, reduce, or swap.
- **Hard info check** — won't calculate TDEE until it has your biological sex, age, height, weight, and activity level.
- **Science-backed** — Mifflin-St Jeor BMR, safe calorie floors (1200F / 1500M / 1600 teens), protein targets (1.2-1.6g/kg/day), real plateau diagnostics.

## How It Works

The GPT uses a system prompt (`gpt-instructions.md`) that defines its persona and behavioral rules, plus a coaching playbook (`coaching-playbook.md`) and reference documents as its knowledge base.

### Scenario Handling

| Situation | What It Does |
|-----------|-------------|
| "Here's what I ate today" | Structured food log with confidence tags, liquid-calorie flags, running daily totals |
| "Make me a week of meals" | 7-day plan with shared ingredients, batch-cook instructions, consolidated grocery list |
| "I'm going to [restaurant]" | Top 3 menu picks by goal-fit with specific ordering scripts ("dressing on the side, swap fries for veggies") |
| "What can I make with this?" | 2-3 options from pantry / fridge photo at different effort levels |
| Social eating pressure | Pre-event strategy + practiced scripts to decline pushy offers without drama |
| Binge / overeat | Empathy, normalize, weekly reframe, find the trigger |
| Plateau | Diagnostic checklist (tracking? TDEE? exercise? sodium? cycle?) |
| Emotional eating | HALT self-check, then alternatives before eating |
| Scale panic | "1 lb fat = 3,500 extra cal. Did that happen? If not, it's water." |
| Unrealistic goal | Honest math + explain why rapid loss backfires. Refuses unsafe deficits. |
| "What do I eat?" | 30g protein + 10g fiber framework with concrete examples |
| Repeat patterns | Names the pattern on the 3rd occurrence — challenges without shaming |
| End of a chat window | Generates a State Snapshot you paste into the next conversation |

## Repo Structure

```
.
├── gpt-instructions.md        # GPT system prompt (paste into GPT Builder)
├── coaching-playbook.md        # Knowledge doc: scenarios, HALT, science numbers
├── CLAUDE.md                   # Product philosophy & feature roadmap
└── reference/                  # Source knowledge documents
    ├── advice.txt              # 110lb personal loss insights
    ├── reddit-loseit.txt       # r/loseit comprehensive FAQ
    ├── reddit-weightlossadvice.txt  # r/WeightLossAdvice guide
    ├── Calorie Calculator.pdf  # BMR/TDEE formulas & meal plans
    ├── halt self check.pdf     # Kaiser Permanente HALT framework
    └── Dietary Guidelines for Americans 2025-2030.pdf
```

## Build Your Own

1. Go to [ChatGPT GPT Builder](https://chat.openai.com/gpts/editor)
2. Paste `gpt-instructions.md` into the **Instructions** field
3. Upload all files from `reference/` plus `coaching-playbook.md` as **Knowledge**
4. Set conversation starters:
   - "How can I lose weight healthily?"
   - "What are some effective exercises for weight loss?"
   - "Can you suggest a balanced diet plan?"
   - "How many calories should I eat to lose weight?"
5. Publish

## Key Science

| Fact | Number |
|------|--------|
| Safe loss rate | 1-2 lbs (0.5-1 kg) / week |
| Calorie deficit | 250-500 cal below TDEE |
| 1 lb of fat | ~3,500 calories |
| Daily water weight swing | 3+ lbs (normal) |
| Weight loss split | ~80% diet, ~20% exercise |
| Protein target | 1.2-1.6g per kg body weight / day |
| Regain rate without maintenance | 80% within 3-5 years |
| Exercise machine overestimate | 25-33% |
| Muscle loss without resistance training | 20-33% of weight lost |

## References

- [How Real People Use ChatGPT to Lose Weight — NanoRhino](https://nanorhino.com/blog/how-real-people-use-chatgpt-to-lose-weight-reddit-research) — 30+ Reddit case study that shaped this GPT's behavioral design
- [r/loseit FAQ](https://www.reddit.com/r/loseit/wiki/faq/) — comprehensive weight loss community knowledge
- [Kaiser Permanente HALT Framework](https://healthy.kaiserpermanente.org/) — emotional eating self-check
- [Dietary Guidelines for Americans 2025-2030](https://www.dietaryguidelines.gov/) — federal nutrition recommendations
- [Mifflin-St Jeor Equation](https://en.wikipedia.org/wiki/Basal_metabolic_rate#BMR_estimation_formulas) — most accurate BMR formula for general population

## License

MIT — use it, modify it, build on it.
