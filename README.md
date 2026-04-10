# Weight Loss Nutritionist GPT

An AI-powered weight loss coach that goes beyond calorie counting. Built as a custom GPT with evidence-based nutrition science, behavioral psychology (HALT framework), and a coaching tone that keeps people going instead of making them quit.

**[Try it free on ChatGPT](https://chatgpt.com/g/g-69d902da41448191b094b5dc57ec331b-weight-loss-nutritionist)**

## What Makes It Different

Most diet GPTs are glorified calorie calculators. This one actually coaches:

- **Empathy first, numbers second** — validates feelings before giving advice. When you overeat, it reframes to the weekly view instead of guilt-tripping you.
- **HALT framework** — catches emotional eating by checking if you're actually Hungry, or just Angry, Lonely, or Tired (based on Kaiser Permanente's behavioral model).
- **ADD / REDUCE / REPLACE** — never tells you to stop eating something. Instead suggests what to add, reduce, or swap. Restriction doesn't work long-term.
- **Hard info check** — won't calculate TDEE until it has your biological sex, age, height, weight, and activity level. No guessing.
- **Science-backed** — Mifflin-St Jeor BMR, safe calorie floors (1200F/1500M/1600 teens), protein targets (1.2-1.6g/kg/day), and real plateau diagnostics.

## How It Works

The GPT uses a system prompt (`gpt-instructions.md`) that defines its persona and behavioral rules, plus a coaching playbook (`coaching-playbook.md`) and reference documents as its knowledge base.

### Scenario Handling

| Situation | What It Does |
|-----------|-------------|
| Binge / overeat | Empathy, normalize, weekly reframe, find the trigger |
| Plateau | Diagnostic checklist (tracking? TDEE? exercise? sodium? cycle?) |
| Emotional eating | HALT self-check, then alternatives before eating |
| Scale panic | "1 lb fat = 3,500 extra cal. Did that happen? If not, it's water." |
| Unrealistic goal | Honest math + explain why rapid loss backfires |
| "What do I eat?" | 30g protein + 10g fiber framework with concrete examples |

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

- [r/loseit FAQ](https://www.reddit.com/r/loseit/wiki/faq/) — comprehensive weight loss community knowledge
- [Kaiser Permanente HALT Framework](https://healthy.kaiserpermanente.org/) — emotional eating self-check
- [Dietary Guidelines for Americans 2025-2030](https://www.dietaryguidelines.gov/) — federal nutrition recommendations
- [Mifflin-St Jeor Equation](https://en.wikipedia.org/wiki/Basal_metabolic_rate#BMR_estimation_formulas) — most accurate BMR formula for general population

## License

MIT — use it, modify it, build on it.
