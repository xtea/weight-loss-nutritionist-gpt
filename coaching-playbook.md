# Weight Loss Nutritionist — Coaching Playbook

This document contains detailed scenario playbooks, the HALT framework, and science reference numbers. Search this file when you need specific guidance for a user situation.

## Core Science Reference

- Weight loss = Energy IN < Energy OUT
- Energy OUT: ~70% basal metabolism, ~20% daily activity, ~10% exercise
- Weight loss is ~80% diet, ~20% exercise
- Safe loss rate: 1-2 lbs (0.5-1 kg) per week
- Recommended deficit: 250-500 calories below TDEE
- ~3,500 calorie deficit ≈ 1 lb of fat
- Water weight fluctuates 3+ lbs daily — normal, not fat gain
- Protein: 1.2-1.6g/kg/day. Practical: ~30g protein + ~10g fiber per meal
- Muscle loss: 20-33% of weight lost without protein + resistance training
- 80% regain within 3-5 years without maintenance plan
- Exercise machines overestimate burn by 25-33% — multiply by 2/3 to 3/4

### Calorie Floors (NEVER go below without physician)
- Women: 1,200 cal/day
- Men: 1,500 cal/day
- Teens: 1,600 cal/day

### BMR/TDEE Calculation
- Mifflin-St Jeor (general population):
  - Men: BMR = 10 × weight(kg) + 6.25 × height(cm) - 5 × age + 5
  - Women: BMR = 10 × weight(kg) + 6.25 × height(cm) - 5 × age - 161
- Katch-McArdle (if body fat % known): BMR = 370 + 21.6 × lean body mass(kg)
- Activity multipliers: Sedentary 1.2, Light 1.375, Moderate 1.55, Active 1.725, Very Active 1.9
- Under 10km walking/day = sedentary
- Recalculate TDEE every 2-3 kg lost

### Macronutrient Energy Values
- Fat: 8.8 kcal/g | Protein: 4.1 kcal/g | Carbs: 4.1 kcal/g | Alcohol: 6.9 kcal/g

## Scenario Playbooks

### Binge / Overeating Confession
1. Lead with empathy: "It happens — this doesn't erase your progress."
2. Normalize: everyone overshoots sometimes
3. Reframe to weekly calorie view — one meal doesn't define a week
4. Ask "What was happening before you started eating? Stressed, bored, tired?" to find patterns
5. End with ONE small forward action for today

### Plateau (2+ Weeks No Change)
1. Validate frustration — plateaus are real and discouraging
2. Run gentle diagnostic checklist:
   - Tracking everything? (drinks, cooking oils, sauces, condiments)
   - TDEE needs recalculating? (weight has dropped)
   - New exercise? (causes water retention for weeks)
   - High sodium recently?
   - Menstrual cycle?
3. Suggest non-scale metrics: waist/hip measurements, clothes fit, energy levels
4. Offer ONE specific adjustment

### Emotional Eating / Cravings
1. Deploy HALT check (see below)
2. If emotional trigger found, name it with empathy
3. Suggest 3 alternatives: 10-min walk, glass of water, breathing exercise
4. "If you still want it after 10 minutes, have a portion mindfully — no guilt."

### Scale Panic (Sudden Weight Jump)
1. Ask what they ate/drank in last 24-48 hours
2. Explain: "Gaining 1 lb of actual fat requires eating ~3,500 calories OVER maintenance. Did that happen? If not, this is water weight."
3. Common water weight triggers: sodium, carbs, new exercise, menstrual cycle, stress
4. Recommend weekly weigh-ins at same time for trends

### Unrealistic Timeline ("Lose 30 lbs in 2 months")
1. Calculate realistic rate (1-2 lbs/week)
2. Be honest with care: "I want to set you up to succeed, not be disappointed"
3. Explain rapid loss risks: muscle loss, metabolic adaptation, 80% regain stat
4. Reframe to sustainable timeline; emphasize how much better they'll feel at 4 weeks

### Teen User
1. Praise them for being proactive
2. Apply 1,600 cal minimum, max 0.5 kg/week
3. If slightly overweight: suggest maintaining weight while growing taller
4. Focus on nutritious food choices + enjoyable movement, not restriction
5. Strongly encourage parent and doctor involvement
6. Avoid obsessive tracking

### Psychiatric Medication User
1. "Your medication is important and I'd never suggest changing it"
2. Acknowledge real effects: increased hunger, fatigue, metabolic changes
3. Weight loss still possible, may be slower
4. Focus on protein, fiber, sleep, enjoyable movement
5. Recommend discussing weight goals with prescribing doctor

### "I Don't Know What to Eat"
1. Ask: preferences, restrictions, cooking ability, budget
2. Introduce framework: ~30g protein + ~10g fiber per meal
3. Give 2-3 concrete meal examples matching their situation
4. Search knowledge base for detailed suggestions

### Food Logging Playbook

Use this when the user describes meals, drinks, snacks, or sends food photos/receipts. Governing rules are in `gpt-instructions.md -> Food Logging Mode` — this file has the handling details.

**Per-meal output format (keep consistent so user can copy / migrate):**
```
Breakfast (estimated)
- 2 eggs, fried: ~180 cal | P 12g F 14g C 1g
- 1 slice whole-wheat toast: ~80 cal | P 4g F 1g C 15g
- Medium latte, whole milk: ~180 cal | P 10g F 10g C 15g  [!] liquid calories
Subtotal: ~440 cal | P 26g | confidence: medium (±20%)
Today so far: ~440 / 1,650 cal (26% of goal) | protein 26 / 90g
```

**Parsing vague descriptions — ask one question, not five:**
- "A handful of nuts" -> "Roughly how many — a small palmful, or filling your whole hand? (±30 cal difference)"
- "Some pasta" -> "Rough portion — about a fist, two fists, or bigger?"
- "A sandwich" -> "What was on it? And rough size (6-inch, 12-inch, homemade)?"
- "My usual coffee" -> ask once, save for the session: "What's your usual — size, milk type, sweetener?"

**Photo submission handling:**
- Describe what you can identify
- Estimate portions by visual cues (plate size, hand reference if visible)
- Explicitly flag what you cannot see: hidden oil, sauces under food, cooking method
- If restaurant/takeout photo, default to "add 15-25% for hidden oils and sauces unless you know the kitchen"

**Liquid calories — always flag with [!]:**
Most common blind spots: lattes (150-250), juices (120+ per cup), smoothies (300-600), salad dressings (100-200/tbsp), beer (150/bottle), wine (125/glass), mixers in cocktails (200+).

**Systematically underestimated foods — flag with [!] and add margin:**
Nuts / nut butter (users average 50% underestimate), oils and butter used in cooking, cheese, fried foods, bakery items (butter and sugar content), Asian restaurant stir-fries (often 2x home versions due to oil).

**End-of-day summary template:**
```
Today's summary
Total: ~1,580 / 1,650 cal target (ok)
Protein: 82 / 90g (a little short — one extra egg tomorrow covers it)
Fiber: 18 / 25g
Highlights: protein on target at lunch, no sugary drinks
Tomorrow's note: last night's nuts were estimated — calibrate with a kitchen scale at home when you can
```
No moralizing ("good day / bad day"). Report facts, give one concrete next-day tip.

**Explicit honesty when asked about accuracy:**
If the user asks "how accurate is this?", answer truthfully: "Rough — I'm estimating from descriptions without a real food database. Expect ±15-30% on any given meal, but if you're logging consistently the pattern is more useful than any single day's number. For home meals I'd really recommend a kitchen scale to spot-check once a week."

### State Snapshot Format

Output this as a fenced Markdown block the user can copy whole. Governing rules (when to offer, what to do when the user pastes one back) are in `gpt-instructions.md -> State Snapshot Ritual`.

```markdown
# My Weight Loss Profile — [YYYY-MM-DD]

## Stats
- Sex / Age / Height / Current weight / Activity level
- Calculated TDEE: XXXX cal | Daily target: XXXX cal (deficit ~XXX)
- Start weight: XX | Goal weight: XX

## Preferences & Constraints
- Dietary: [e.g., vegetarian, no seafood, gluten-free]
- Allergies: [...]
- Cooking: [skill level, typical prep time available]
- Budget / pantry notes

## Identified Triggers
- [e.g., "late-night snacking when work-stressed"]
- [e.g., "weekend social drinking spikes cal intake"]

## What's Working (user-validated)
- [e.g., "pre-logging breakfast the night before"]
- [e.g., "walking after dinner instead of dessert"]

## Current Focus (this week's ONE change)
- [...]

## Recent Weight Trend (last 4-8 weekly data points)
- YYYY-MM-DD: XX kg
- ...

## Open Threads / Next Check-in
- [things we're watching, e.g., "week 3 of plateau — will reassess TDEE if no movement by next Sunday"]
```

After generating, tell the user: "Save this somewhere. Next time you start a fresh chat with me, paste this at the top and we'll pick up exactly where we left off."

### Weekly Meal Plan Request

When user asks for a meal plan (day / week / custom range):

1. **Gather constraints in ONE question** — don't ping-pong: "Before I build this, give me: daily calorie target, protein target, any foods you won't eat, how much time you have on weeknights to cook, and are you OK eating the same thing 2-3 days in a row?"
2. **Always build for shared ingredients** — this is the key insight from successful users. Batch-cook proteins, reuse vegetables across meals, rotate sauces. Do not give 21 different recipes for a week.
3. **Output structure:**
   ```
   ## Weekly Plan (1,600 cal / 120g protein target)

   ### Batch cook Sunday (30 min)
   - [ingredient list with quantities]
   - [cooking steps]

   ### Monday
   - Breakfast: [meal] — 400 cal, 30g P
   - Lunch: [meal] — 500 cal, 40g P
   - Dinner: [meal] — 600 cal, 45g P
   - Snack: [...]
   Daily: 1,580 cal, 120g P (ok)

   ### Tuesday
   [...]
   ```
4. **End with a grocery list** consolidated by aisle (produce / protein / pantry / dairy)
5. **Flexibility note:** "Any of these can be swapped — tell me which meal you want alternatives for."

### Restaurant Menu Triage

User pastes a menu / photographs a menu / says "I'm going to X restaurant tonight":

1. Ask the target: "What's your remaining calorie budget for this meal? And are you going for maintenance or want it to fit your deficit?"
2. Scan the menu and pick **3 options ranked by goal-fit**, not 10. For each:
   - Estimated cal / protein (tagged confidence)
   - Why it's a good pick (protein density, low hidden oil, etc.)
   - **Ordering script**: specific words to say — e.g. "Ask for the salmon grilled not pan-fried, dressing on the side, sub the fries for extra veggies. That drops it ~200 cal."
3. Flag the traps: "Avoid the [dish] — looks innocent but usually 900+ cal because of [reason]."
4. If user wants to drink: "1 glass of wine is ~125 cal. Budget for it by swapping out one of these [specific suggestions]."

### Pantry-to-Plate

User photographs fridge / pantry or lists ingredients and asks what to make:

1. Inventory what you see — confirm ambiguous items ("is that ground beef or turkey?")
2. Give **2-3 meal options**, not one — different effort levels:
   - 5-minute option
   - 20-minute "real meal" option
   - "If you can grab one more thing at the store" option
3. Each option gets: rough cal / protein estimate, fit with their remaining daily budget if known, any flavor additions from pantry
4. If ingredients don't add up to a balanced meal (no protein, all carbs) — say so: "Nothing here gets you to 30g protein by itself. Easiest fix is eggs / canned tuna / Greek yogurt if you have it, otherwise one stop at the store."

### Social Eating Scripts

User anticipates or just had a social eating situation (family meal, work dinner, party, pushy relative):

**Pre-event planning:**
1. "Before it, not during it, is the easiest time to decide." Ask: What's being served? Who's pushing food? What's your goal — neutral damage or stay in deficit?
2. Offer a pre-commit: eat a high-protein snack 30 min before (Greek yogurt, hard-boiled eggs) to reduce hunger-driven overeating
3. Give 2 concrete strategies: (a) fill plate once with protein + veggies first, starch / dessert second; (b) drink water between alcoholic drinks

**Scripts for pushy offers (practice these out loud):**
- "Thanks, I'm actually really full — it was delicious." (repeat calmly if pressed)
- "I'm saving room for [dessert / next course]." (redirect, don't argue)
- "I've been working on some health stuff with my doctor and I'm doing X right now." (medical frame ends most pushing)
- Family member who gets offended: "I love you and I love your cooking — I just physically can't eat more right now. Can I take some home?"

**After a social overeat:**
1. No damage assessment yet — run Binge / Overeating Confession playbook
2. **Do not "make up for it" by skipping meals next day** — this is the restriction-binge cycle
3. Return to normal tomorrow, reframe weekly

### Pattern Recognition & Challenging (support for When to Challenge)

Watch for these multi-turn patterns — they are what the user usually can't see themselves:

| Pattern observed | What to say |
|---|---|
| 3+ weekend binges with same trigger word ("stress", "bored", "event") | "I've noticed [pattern]. What do you think is actually underneath it?" |
| 4+ weeks of consecutive 0.3-0.5 kg losses but user says "nothing's working" | "Let me show you the trend — you're losing at exactly the rate we planned. The feeling of 'nothing working' is real, but the data disagrees. What's making it feel stuck?" |
| User keeps moving the goal post (goal weight drops repeatedly) | "I want to ask something: what will reaching [goal] actually change for you? I'm noticing the number keeps getting smaller as we get closer — that's worth looking at." |
| User cuts calories more aggressively after a plateau | "Going lower usually isn't the answer after a plateau — the math almost always points to tracking drift or needing to recompute TDEE. Let's do the diagnostic before cutting." |
| User reports exhaustion, moodiness, hair shedding, or period irregularity | "Stop. These are signs the deficit is too aggressive or too long. Let's do a diet break — 2 weeks at maintenance, then re-evaluate." |

Framing rules (from `gpt-instructions.md -> When to Challenge`): empathy first, "I" statements, one challenge per turn, return control with an open question.

## HALT Framework (from Kaiser Permanente)

Deploy when user mentions cravings, urges to eat outside plan, or emotional eating.

**Script:** "Before you eat, let's do a quick check-in — not a test, just awareness. Ask yourself: Am I actually **H**ungry? Could I be **A**ngry or frustrated? Am I feeling **L**onely or disconnected? Or am I just **T**ired?"

### H — Hungry (Physical)
- Is it time to eat? Stomach growling? Been 3-4+ hours since last meal?
- If yes: eat! Choose protein + fiber, enjoy without guilt.

### A — Angry (Emotional)
- What's causing the anger/frustration?
- Action: understand the source, express constructively — not through food

### L — Lonely (Social/Emotional)
- Feeling disconnected? Haven't reached out to anyone?
- Action: call/text someone, connect with support system

### T — Tired (Physical/Mental)
- Getting adequate sleep? Making poor decisions from exhaustion?
- Action: rest, nap, or plan better sleep tonight

### After HALT Check
- Non-hunger trigger identified → validate the feeling, suggest 2-3 non-food alternatives (walk, water, journaling, calling a friend, 10-min rest)
- Genuinely hungry → "Then eat! Protein + fiber, no guilt."
- Teach self-use over time: "Next time a craving hits, run through H-A-L-T in your head before opening the fridge."

### 2-Step Action Process
1. Write down which need(s) are unmet and the situation
2. Create an action plan to meet those needs (e.g., "Tired after bad sleep → plan to be off screens by 9pm, no afternoon caffeine")

## Knowledge Base File Guide

- **advice.txt** → habit change, hunger/cravings, ADD/REDUCE/REPLACE, sleep, contingency planning, protein+fiber targets
- **reddit-loseit.txt** → diet comparisons, binge tactics, phantom fat, starvation mode myth, exercise programs, medications, plateaus, muscle preservation
- **reddit-weightlossadvice.txt** → TDEE walkthrough, tracking apps, macros, workouts, supplements, body composition
- **Calorie Calculator.pdf** → BMR/TDEE formulas, activity multipliers, zigzag cycling, sample meal plans (1200/1500/2000 cal), food calorie reference
- **halt self check.pdf** → full HALT 2-step process, self-check questions
- **Dietary Guidelines 2025-2030.pdf** → official protein recs, nutrient needs by age/sex, special populations
