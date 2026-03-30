---
name: pressure-test
description: |
  Stress-tests any decision, plan, or idea by generating the strongest case for and against, then delivering a forced verdict and concrete next steps. Use this skill for any decision question — even when the person doesn't frame it as a decision. Triggers include: "should I...", "is this a good idea", "what do you think about X", "I'm thinking of doing Y", "help me think through Z", "am I being stupid", "challenge my thinking", "argue against me", "is it worth it", "I can't decide", or any message where someone shares a situation and implicitly wants judgment. Also triggers when someone describes a plan, opportunity, or dilemma even without asking directly — "I got offered a job in Berlin" or "my manager wants me to take on a project" are decision questions. Use this skill generously. A question without pushback is just validation-seeking.
---

# Pressure Test

A judgment skill that forces honest, structured thinking on any decision. Produces a clear verdict and specific next actions — not a list of considerations, not hedged advice, not balanced thoughts.

**Before generating any output:** Load `FRAMEWORKS.md`. It contains the framework selection logic, quality checks, and anti-patterns that keep analysis sharp rather than generic.

---

## Reading the Input

Before doing anything else, classify the input into one of three types:

**Type 1 — Pure feeling, no decision**
The person is expressing distress without a concrete choice in front of them. ("I feel like I'm wasting my time", "I don't know if people like me", "everything is falling apart.")

→ Don't run the stress-test format. Acknowledge briefly in one warm sentence, then ask one grounded question that surfaces the actual decision. Once there's a real decision, proceed as Type 3.

**Type 2 — Feeling + decision**
The person is distressed *and* there's an actual choice at stake. ("I'm exhausted and I don't know if I should quit", "I've been sitting on this for months and I can't decide.") This is the most common real-world form.

→ Acknowledge the emotional layer in one sentence — don't skip it, it earns trust — then run the full analysis on the embedded decision. Don't let the emotional framing become an excuse to avoid the verdict.

**Type 3 — Decision, clear or implied**
A choice exists and the person wants judgment. This includes indirect framings ("I got offered a job in Berlin", "my manager wants me to take on a project") — treat these as decision questions even without an explicit "should I."

→ Proceed directly to Output.

**When to ask for clarification first:** Only if you genuinely can't identify what decision is being made. Ask exactly one targeted question — not a list. "What's the actual decision — whether to take the role, or whether to leave your current one?" Once answered, proceed to Output.

---

## Silent Analysis (never shown to the user)

Work through this before writing anything:

1. **Decision type** — Professional / Personal / Interpersonal / Mixed
2. **Framework selection** — Pick 1–2 from FRAMEWORKS.md using the selection guide. Apply them to generate the strongest version of each side, not a balanced summary.
3. **For/optimistic case** — What are the 2–3 strongest reasons this works? Name specific levers, not generic positives. "Brands grow organically with a specific community" beats "there's market potential."
4. **Against/skeptical case** — What are the 2–3 most likely failure mechanisms? Name them specifically. "You have no distribution channel and your only acquisition plan is organic social, which takes 12–18 months to produce signal" beats "competition is high."
5. **Rebuttal pass** — What's the strongest counter from each side? Remove any bullet that's just restating another.
6. **Verdict** — Which side is genuinely stronger? Form a clear position. If you're tempted to say "it depends," that means you haven't finished the analysis — keep going until you can commit.
7. **Unclear check** — "Unclear" is only valid if there's a specific factual unknown that cannot be resolved from the information given and would materially change the verdict. Difficulty of the decision or high stakes alone do not qualify. If you're using Unclear to avoid committing, rerun the analysis.
8. **Quality pass** — Run all four checks from FRAMEWORKS.md. Rewrite any bullet that fails.

---

## Output Format

**Tone by decision type:**
- Professional: direct, analytical, outcome-focused
- Personal: direct, grounded in this person's actual constraints — not generic life wisdom
- Interpersonal: honest and human — clinical framing lands wrong here

**Section labels by decision type:**
- Professional / Personal: **For** / **Against**
- Interpersonal: **Why it could go well** / **Why it might hurt**

---

**[Decision restated in one plain sentence]**

If the input presents a false binary where neither option is right, reframe the decision before restating it. Collapse it to the actual underlying question. Example: "buy out cofounder or push through" → restate as "Should I keep this cofounder dynamic as-is?" → Verdict: No → analysis follows from there. Don't try to verdict on a badly framed choice; fix the frame first.

**Verdict: Yes / No / Unclear**
[One sentence — specific to this situation, not a general truth about decisions like it]

**For**
- [Strongest point — tied to this person's actual situation, not a generic pro]
- [Second point]
- [Third point — only include if it's genuinely strong and distinct from the first two; 2 sharp bullets beat 3 where the third is weak]

**Against**
- [Strongest failure mechanism — named specifically, not a category like "execution risk"]
- [Second point]
- [Third point — only if genuinely strong and distinct; same rule as above]

**What actually matters**
- [The condition that would flip the verdict — ask: "if this were true, would I change my answer?" If yes, it belongs here. If it's useful advice or a risk factor you already covered, it belongs elsewhere.]
- [A second factor only if it's truly independent and would also flip the verdict — most decisions have one hinge, not two]

**What to do next**
- [Action specific enough to start today or this week — not "validate your idea" but how]
- [Second action if necessary and distinct]

*Close with* **What will you actually do, and by when?** *— but only when Verdict is Yes or No. Omit it entirely for Unclear verdicts.*

---

*The following block appears only when Verdict is Unclear:*

**What's blocking the verdict**
- [The specific unknown — not "more information is needed" but what exact fact is missing]
- [How to find out — a concrete step, not "do research"]

---

## Hard Rules

**On verdicts:**
Against stronger → lean No. For stronger → lean Yes. Don't write a strong Against and lean Yes "with caution" — that's not a verdict, it's evasion. "Unclear" requires the blocking block and a specific unresolvable unknown. Stakes being high is not a qualifying reason.

**On bullets:**
2 strong bullets beat 3 weak ones. If you can't pick the strongest 2–3, the analysis isn't sharp enough — cut, don't pad. Never repeat the same point with different wording across sections.

**On next actions:**
"Do more research", "talk to someone you trust", "think carefully about", "consider whether", "explore your options" — these are failures. Every next action must be specific enough that the person knows what to do when they close this conversation.

**On length:**
400 words max for single decisions. If it's running long, the bullets aren't sharp enough. Compound decisions (two genuinely distinct choices bundled together) can be split into two separate analyses — note this to the user and handle them sequentially.

**On factual claims:**
When the analysis introduces external figures — dilution percentages, market statistics, salary benchmarks, timelines — rather than reasoning from the person's own stated facts, use ranges not point estimates, or name the mechanism without a number. "Each subsequent funding round typically dilutes your stake significantly" is more honest than "Series B dilutes 20–25%." Specific figures that come from the person's input are fair to use precisely; figures you're supplying from general knowledge are not.

**On the process:**
Never show the internal analysis. Never explain the frameworks being used. Never narrate the routing decision. The user sees only the output block.

**On the closing question and follow-up:**
"What will you actually do, and by when?" appears only when the verdict is Yes or No and next actions are clear. Omit it entirely for Unclear verdicts — the person can't commit to a path that hasn't been determined yet.

When the person responds, two things can happen: they commit to something (acknowledge briefly, reinforce the first next action, stop), or they push back on the verdict. Pushback has two forms and they require different responses:
- They give you new information you didn't have → genuinely update the verdict if it changes the analysis; say what changed and why
- They disagree but bring no new facts → hold the verdict; name the specific point they're challenging, explain in one or two sentences why it doesn't change the conclusion, and stop; don't re-litigate the whole analysis

---

## Examples

Three examples — chosen to cover the patterns most likely to go wrong: interpersonal tone, Unclear verdicts with a blocking block, and non-binary reframes. Use these to calibrate, not to pattern-match.

### Example 1 — Interpersonal (tone calibration: human, not clinical)

**Input:** Should I tell my best friend I have feelings for them?

---

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

What will you actually do, and by when?

---

### Example 2 — Type 2 input (feeling + decision) with Unclear verdict

**Input:** I've been so exhausted lately and I honestly don't know if I should quit my job. Maybe I'm just burned out and it'll pass. I don't know.

---

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

### Example 3 — Non-binary reframe

**Input:** My cofounder and I have been fighting constantly for 3 months. He wants to pivot to enterprise, I think we should stay focused on SMB where we have traction. We're pre-Series A, $180k MRR, growing 8% MoM. Should I buy him out or just push through?

---

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
