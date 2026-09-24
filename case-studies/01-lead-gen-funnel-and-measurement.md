# Case 1 · Lead-gen funnel and measurement

**Client**: a local fitness and swimming center in Southern Italy (anonymized).
**Engagement**: paid, four months (August to December 2026). My scope: paid ads and tracking.
Organic social was handled by a business partner.
**Offer**: a seasonal free-enrollment promotion, valid for people who signed up online and
visited the center within the offer window.

## Results (24 August to 21 September 2026)

| Metric | Real (reconciled) | What the ad platform reported |
|---|---|---|
| Spend | €579.93 | €579.93 |
| Leads (unique people) | **39** | 27 |
| Cost per lead | **€14.87** (target: €30) | €21.48 |
| Leads who also booked a visit | **62%** (measured on 21 leads, 26 Aug to 9 Sep) | not visible |

The platform under-reported real leads by about 30%. The reason is structural, not noise: only
about **15% of sessions** accepted cookies (measured on server logs, 19 to 22 September), so the
platform saw a small share of the people who converted.

## 1. First, a success metric I could trust

A cost per lead computed on the platform's count would have been wrong by a third, and every
budget or creative decision built on it would have inherited the error. So the core metric
became **real leads**: every submission reconciled across the form's own data, a server-side
backup and server logs, one row per unique person. Platform numbers stayed useful for delivery
signals (reach, click cost), never for deciding what works.

## 2. Experiments, one variable at a time

- **4 test cycles on 10 ad concepts**, with a fixed €150 test budget, one variable per test:
  almost always the hook (the angle of the message), with the visual style kept constant.
- **The best ad was not the one with the best click-through rate.** One concept reached the
  highest CTR of the account (1.28%) and the worst conversion: 3 real leads on 280 clicks,
  €42.38 per lead, 1.1% click-to-lead. I paused it. Inside an ad set the algorithm optimizes for
  what it can see (clicks and engagement), so with low consent the choice between variants has to
  come from the real-lead sheet.
- **An honest urgency hook** (the real offer deadline) converted 5.7% of clicks into leads in its
  test, about double the account's historical rate. Small sample (2 leads), so it went to scaling
  with a fallback ready, not as a proven winner.
- **What didn't work, also recorded**: a "stop procrastinating" angle failed in two independent
  tests and was retired; a brand-new AI-generated visual was starved by the delivery algorithm
  from day one against the proven style.

## 3. Diagnosis before action

- **Cost per lead rising**: I split it into click cost and click-to-lead conversion. The whole
  increase came from click costs (seasonal media prices and ad fatigue), while conversion held at
  2.6 to 2.9%. The fix belonged in the ads (new hooks), not in the landing page.
- **Audience**: ages 25 to 34 were the weakest segment in three independent windows, 45 to 54 the
  strongest. I narrowed targeting to 35 to 54 only after two windows agreed, not after one test.
- **Placements**: one placement took 46% of the budget with the lowest CTR (0.67%) and a cost per
  lead about three times the average, over more than 71,000 impressions. I excluded it; the best CTR
  (1.52%) came from a placement receiving 6% of the budget.

## 4. Landing page and QA before launch

- **Message match**: the page did not mention the offer that the ads promised. Headline and
  subtitle were rewritten (four iterations, one discarded for being too long on mobile).
- **Business rules first**: the offer required two conditions together (online sign-up AND a
  visit within the window). The copy says "sign up", not "start", because one service opened only
  after the deadline.
- **QA pass**: legal pages created and linked, links tested from every page, layout checked at
  375, 768 and 1440 px. A navigation bug that had never been tested from secondary pages was found
  and reported.

## Takeaways

- The metric comes first. If the number is wrong, every optimization is wrong with confidence.
- Test one thing at a time and decide on outcomes, not on the proxy that is easiest to see.
- Say the limits out loud: these are leads, not paying members, and conversion to members is not
  tracked.
