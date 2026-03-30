# Pressure Test — A Claude Skill for Real Decisions

Most AI responses to "should I do X?" give you a list of things to consider. This skill gives you a verdict.

**Pressure Test** stress-tests any decision by generating the strongest case for and against, then committing to a clear Yes / No / Unclear with specific next actions you can take this week — not balanced thoughts, not hedged advice, not things to reflect on.

---

## What it does

- Classifies your input (clear decision, decision buried in emotion, or pure feeling with no decision yet) and handles each correctly
- Selects the right analytical framework for the decision type — career vs interpersonal vs financial vs mixed
- Produces a verdict that follows from the analysis, not one that softens at the end
- Names the specific next action you can take today or this week
- Handles pushback: updates the verdict if you bring new information, holds it if you just disagree

---

## When it works best

- Career and business decisions: job offers, quitting, cofounders, startups, stretch projects
- Financial decisions: salary tradeoffs, equity, investments, spending
- Personal decisions: habits, life changes, moves, big commitments
- Interpersonal decisions: whether to say something, relationship choices, conflict

**When it works less well:** highly technical architecture or engineering decisions ("should I use Postgres or MongoDB?") where domain-specific tradeoffs matter more than judgment frameworks. A separate skill for that is in the works.

---

## Examples

### Career decision

**Input**
> My cofounder and I have been fighting constantly for 3 months. He wants to pivot to enterprise, I think we should stay focused on SMB where we have traction. We're pre-Series A, $180k MRR, growing 8% MoM. Should I buy him out or just push through?

**Output**

**Should I keep this cofounder dynamic as-is?**

**Verdict: No**
Three months of unresolved strategic conflict at $180k MRR is a company-threatening distraction — and the SMB vs enterprise question is answerable with your own data right now, which means the fight is already past its expiry date.

**For resolving it (buyout or formal role split)**
- At 8% MoM, you have real traction — that data should settle the strategic question, which either re-aligns you or makes the case for separation cleanly
- Unresolved cofounder conflict is one of the top reasons pre-Series A companies fail to raise; investors will see it before you get to term sheets

**Against pushing through**
- "Pushing through" without resolution means one of you executes a strategy you don't believe in — that person underperforms and resents it, and you'll both know it
- Three months means trust is already eroding; without a structural change, the next conflict arrives faster and hits harder
- You can't split focus between SMB and enterprise motions simultaneously at this stage — the indecision is itself a strategy, and it's a losing one

**What actually matters**
- Whether your current MRR is concentrated in SMB or enterprise — pull the breakdown this week; it's the one fact that turns a values argument into a data argument

**What to do next**
- Pull your customer revenue by segment before the next conversation with your cofounder — if 80%+ is SMB, you have a fact-based case that ends the debate
- If that conversation still doesn't resolve it, engage a startup lawyer to draft buyout terms before your next investor call

**What will you actually do, and by when?**

---

### Decision buried in emotion

**Input**
> I've been so exhausted lately and I honestly don't know if I should quit my job. Maybe I'm just burned out and it'll pass. I don't know.

**Output**

That kind of "maybe it's me, maybe it's the job" uncertainty is the hardest to sit with — and also the most important to resolve before making a move.

**Should I quit this job?**

**Verdict: Unclear**
Burnout and a bad job look identical from the inside; the right answer depends entirely on which one this is.

**For quitting**
- If the exhaustion traces to specific, structural things about this role — the manager, the scope, the hours — staying just extends a diagnosed problem
- Burnout that goes unaddressed long enough shifts from a work problem to a health problem; the cost of staying isn't just career stagnation

**Against quitting**
- Exhaustion that feels ambient and sourceless usually travels — a new job brings relief for 90 days, then the same feeling returns
- Quitting without a role lined up compounds stress rather than relieving it; financial pressure on top of burnout is harder, not easier

**What actually matters**
- Whether you can name the specific things draining you — if you can list them, they're probably job-specific; if it all blurs together, the source is likely internal

**What's blocking the verdict**
- Whether the exhaustion is job-specific or portable: for the next 5 workdays, write down at the end of each day what specifically drained you. If the same 2–3 things appear every day and they're inherent to this role, quit. If the list is different every day or points to things that would follow you anywhere, don't.

---

### Interpersonal decision

**Input**
> Should I tell my best friend I have feelings for them?

**Output**

**Should I tell my best friend I have feelings for them?**

**Verdict: Yes**
The cost of staying quiet is already compounding, and unexpressed feelings at this intensity rarely stay contained without changing the friendship anyway.

**Why it could go well**
- Friendships that survive honesty are usually stronger for it — the ones that can't weren't as solid as they felt
- Your friend gets to make an informed choice about the dynamic; right now only you're carrying it
- Saying it removes the ambiguity that's almost certainly already changing how you show up around them

**Why it might hurt**
- If they don't feel the same there will be an adjustment period — the friendship may change shape even if it survives
- Timing matters: if they're in a difficult place right now, the conversation may land worse than it deserves
- You can't unsay it — if losing the friendship entirely would devastate you, that risk is real and worth sitting with honestly before you speak

**What actually matters**
- Whether you can genuinely handle a "no" without it ending things — be honest with yourself about this before saying anything
- How you say it matters as much as whether you say it — framing it as sharing, not asking for something, changes the pressure on them

**What to do next**
- Have it in person, not over text — they will read the worst version of every word otherwise
- Open with "I want to be honest about something, and I'm not asking you to do anything about it" — it lowers the stakes before the hard part

**What will you actually do, and by when?**

---

## Installation

1. Download `pressure-test.skill` from the [releases page](../../releases)
2. Go to [claude.ai](https://claude.ai) → Settings → Skills
3. Click **Upload skill** and select the downloaded file
4. Done — the skill activates automatically when you ask Claude about any decision

---

## How to trigger it

You don't need a special command. Just describe your decision naturally:

- *"Should I take this job offer?"*
- *"I'm thinking of moving cities — is this a bad idea?"*
- *"My cofounder and I can't agree on direction. What should I do?"*
- *"I've been offered equity instead of salary. Help me think through this."*
- *"I don't know if I should say something to my manager about this."*

The skill also catches indirect framings — *"I got offered a job in Berlin"* triggers it just as well as *"should I move to Berlin?"*

---

## Repo structure

```
pressure-test/
├── SKILL.md          # Core skill instructions and examples
├── FRAMEWORKS.md     # Decision framework reference (Pre-Mortem, Reversibility Test, etc.)
├── pressure-test.skill  # Packaged file for installation
└── README.md
```

`SKILL.md` contains the routing logic, output format, and hard rules. `FRAMEWORKS.md` contains the six analytical frameworks the skill selects from based on decision type, plus the anti-patterns and output quality checks. Both files are included so you can read, fork, and improve either.

---

## Contributing

Issues and PRs welcome. If you find a decision type that produces weak output, open an issue with the input and what was wrong with the output — that's the most useful contribution. The skill has been tested across career, financial, interpersonal, mixed, vague, and emotional inputs, but real-world edge cases are the best source of improvements.

---

## License

MIT
