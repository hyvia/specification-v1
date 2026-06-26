# Hyvia Website — Content & Structure Spec (v1)

> Hand-off brief for the Webflow build. Target go-live: **July 1** (flex to ~10 days, quality over speed).
> Deliverable rule: **finished, paste-ready copy** + section layout + assets needed.
> Status: 🟢 = locked · 🟡 = drafting · ⚪ = not started

---

## 1. Global

### Primary job of the site
Earn a skeptical pro-club decision-maker's **trust in ~60 seconds** and make it trivial to **book a demo**. Credibility + visibility first; SEO/inbound is opportunistic, not a pillar.

### Primary audience
**Head of Performance / Sports Science / Medical at a professional football club.** Data-literate, skeptical, judges on rigor and proof. Head coach = influencer; board/procurement = approver. Famous players = ambassadors / social proof only — *not* a buyer track.

### Positioning one-liner
> **Hyvia is a fitness-grade team performance & readiness platform — the first to combine wearable vitals with sweat biomarkers (cortisol, lactate, pH), continuously, with AI that forecasts each athlete's next-match readiness.**

### Message pillars (the spine of every page)
1. **See what no one else can** — vitals *plus* sweat chemistry (cortisol, lactate, pH). The unique data.
2. **Continuous, not snapshots** — every training, every day, for months.
3. **AI that forecasts, not just reports** — longitudinal data → next-match readiness & performance. The payoff.
4. **Built for the coach's call** — physical *and* mental stress, readiness, performance score, in one dashboard.
5. **Credible by design** — fitness-grade (like Whoop/Oura), backed by NC State, Innovosens, clinical advisors, and a live pro-club pilot.

### The product = the OUTPUT
The value is the **output to the coach** (readiness, stress, fatigue, recovery, performance score, AI match prediction) — *not* the band, patch, or software. Every page leads with the output; hardware is demoted to "how we capture it."

### Claim rules (NON-NEGOTIABLE guardrails)
- **Fitness-grade, NOT medical-grade.** Position openly alongside Whoop/Oura (the accepted standard). Never imply clinical/diagnostic use.
- **Allowed verbs:** monitor, indicate, flag, support, forecast, anticipate, surface.
  **Banned verbs:** diagnose, prevent, treat, cure, guarantee, "measure clinically."
- **Sweat (cortisol/lactate/pH) = a "first-to-integrate" novelty claim, never a precision claim.** Never publish accuracy percentages.
- **No "neurotech." No "healthcare."** "Mental health" → reframe as **"mental stress" / "stress & recovery."**
- **AI = forecast / decision-support, not a fortune-teller.** Credibility comes from the **data moat** (continuous + longitudinal + sweat chemistry no one else has), not from bold accuracy claims.
- Trend hooks we *do* ride: **AI** and **mental stress** — worded conservatively.
- **Confident, not arrogant.** State the difference as plain fact ("the first to integrate sweat chemistry," "signals no other platform captures") — never "we're the best," never disparage Whoop/Oura. Treat them as the respected category we *extend*, not rivals we beat.

### Brand
Use existing Hyvia corporate/brand identity (colors, logo, fonts already defined). Dark theme. App + dashboard designs available for real screenshots.

### Conversion / CTA
- Primary CTA everywhere = **"Book a demo"** → **short request form**: *name · role · club · work email* → routes to inbound inbox/CRM. Low friction, qualifies the lead.
- Secondary = **"Log in →"** (small) → dashboard subdomain.
- No pricing, no self-serve signup (enterprise, relationship-led sale).

### SEO baseline (opportunistic, not the strategy)
- The sharpest discovery hook is **cortisol** ("nobody tracks cortisol for teams"). Seed it in titles/meta where honest.
- Candidate terms: *cortisol monitoring athletes, sweat lactate tracking, athlete readiness platform, team performance monitoring, player fatigue & stress monitoring.*
- Heavy SEO lifting waits for the **v2 blog/Insights** (case studies + cortisol explainers).

### Product framing — present-tense, with guardrails
Present Hyvia as a **real, present-tense product** — NOT "coming soon." (Visibility site, not a sales engine; no club sale happens before patches ship ~2 months out, so no one is misled into a purchase.)
- **Guardrail 1 — capability in present tense:** "Hyvia reads cortisol, lactate, pH from a sweat patch" ✅ — describe what it does as if live.
- **Guardrail 2 — no commerce/availability claims:** ❌ no "buy now / in stock / order today / ships in X / pricing." A visibility site never needs them.
- **Guardrail 3 — no tech specifics:** generic "sweat patch" only (see naming rules).
- **Effect:** looks fully ready, but makes no literal claim that detonates if a buyer probes.

### Naming & proof rules  (revised — competitive secrecy)
- **External suppliers — DO NOT NAME:** ❌ NC State, ❌ Innovosens. Revealing the supply chain lets competitors approach/poach them. No logos, no "powered by," no mention anywhere on the site.
- **Patch description — generic only:** "a sweat patch / skin sensor" that reads cortisol, lactate, pH. ❌ Never "colorimetric," "microfluidic," or any supplier/tech detail.
- **Internal people — OK to feature (credibility):** ✅ the two medical advisors (named + title + photo + quotes, with consent); ✅ the Head of Performance (internal team). [public quote vs background-only — OPEN]
- **Turkish club:** pilot user (free bands), not a paying flagship. [keep a logo/"top-division club" line vs drop — OPEN]
- Frame all credibility as **background validity**, never the hero of a page.

---

## 2. Sitemap

```
HOME ............. output-led narrative — carries the whole pitch
PLATFORM ......... how it works: band + sweat patches + dashboard + app + data flow (demoted "how")
SOLUTIONS ........ the value/outputs to the coach (the star)
SCIENCE .......... credibility: method, partners, advisors, fitness-grade stance
COMPANY .......... team, advisors, partners, pilot, mission
[Book a demo] .... primary CTA, persistent in nav
[Log in →] ....... secondary, small → dashboard subdomain
        ── v2 ──
INSIGHTS ......... blog / CMS (case studies + cortisol/SEO content)
```

**Nav order:** Platform · Solutions · Science · Company  (swappable — Home already leads with value)

---

## 3. Pages

### 🟡 Home — *(drafting now)*

#### Section 1 — Hero  🟢
- **Intent:** In 3 seconds, say "peak performance you can *foresee*," and look credible enough to scroll.
- **Copy:**
  - Headline: **Peak performance, predicted.**
  - Subhead: *Hyvia gives coaches an AI readiness and performance forecast for every athlete — built on continuous vitals and sweat-based markers like cortisol that reveal true stress and recovery, all in one dashboard.*
  - CTA: `[Book a demo]` (primary)  `[See the science]` (secondary)
- **Layout:** Left = headline/subhead/CTAs. Right = real **coach-dashboard screenshot** (readiness/scores) — NOT the band.
- **Assets:** Hi-res dashboard screenshot showing readiness + a performance/forecast view.

#### Section 2 — Credibility strip  🟡
- **Intent:** Light "background validity" band, just under the hero. No supplier names.
- **Copy (three trust chips):**
  *In use at a top-division European football club  ·  Built with practicing sports-medicine experts  ·  Continuous, fitness-grade monitoring*
- **Layout:** thin full-width strip, muted, three items separated by dots.

#### Section 3 — The Problem  🟡
- **Intent:** Name the coach's pain; set up the wedge. No competitor naming.
- **Copy:**
  - Headline: **You can see how hard a player trained. Not what it cost them.**
  - Body: *Physical load is easy to measure. The hidden cost — accumulating fatigue, rising stress, slipping recovery — stays invisible until it shows up as an injury or a flat performance. Most monitoring captures vitals in snapshots, misses the body's stress chemistry entirely, and tells you what already happened — never what's coming.*
  - ⚠️ Stat callout — **DEFAULT: CUT** unless a real citation is supplied. (Current site's "up to 40%…" has no source on hand.)
- **Layout:** centered statement, optional stat as a large pull-number beside it.

#### Section 4 — The difference (the wedge)  🟡
- **Intent:** The integration no one else brings together. Confident, factual.
- **Copy:**
  - Headline: **A complete read on every athlete — body and mind.**
  - Intro: *Hyvia brings together three things no single platform combines:*
  - Pillar 1 — **Sweat chemistry.** *Cortisol, lactate and pH from a simple sweat patch — a direct read on stress, effort and recovery that vitals alone can't show.*
  - Pillar 2 — **Continuous, not snapshots.** *Every session, every day, building each athlete's true baseline.*
  - Pillar 3 — **AI that looks ahead.** *Turns months of data into a forward-looking readiness and performance forecast — not just yesterday's numbers.*
- **Layout:** headline + three pillars (icon + title + line each).

#### Section 5 — The outputs (Solutions teaser)  🟡
- **Intent:** The value = the output. Tease the Solutions page.
- **Copy:**
  - Headline: **What your coaches actually see.**
  - Intro: *Hyvia turns raw biomarkers into the calls a coach makes every day:*
  - Cards (teaser — full set on Solutions): **Readiness** — *recovered & ready today.* · **Stress** — *physical & mental load.* · **Fatigue** — *chronic strain over time.* · **Performance score** — *how they performed.* · **AI prediction** — *how they'll perform next.*
  - CTA: `[Explore the outputs →]` → Solutions
  - ⚠️ Confirm exact output names against the real dashboard.
- **Layout:** card grid over a dashboard screenshot.

#### Section 6 — How it works (Capture → Analyze → Forecast)  🟡
- **Intent:** The 3-step mechanism (your old triad). Hardware demoted to "Capture."
- **Copy:**
  - Headline: **From the body to the bench, in three steps.**
  - Step 1 — **Capture.** *The Hyvia band and sweat patch read vitals and biomarkers continuously, as athletes train and recover.*
  - Step 2 — **Analyze.** *AI weighs each athlete's live data against months of their own history.*
  - Step 3 — **Forecast.** *Coaches get readiness, stress and performance — plus a forward-looking forecast — in one dashboard.*
  - CTA: `[See the platform →]` → Platform
- **Layout:** 3 horizontal steps with connecting arrows.

#### Section 7 — The science (teaser)  🟡
- **Intent:** Earn trust; route to Science. No supplier names; respectful nod to the category.
- **Copy:**
  - Headline: **Grounded in real science.**
  - Body: *Hyvia is built with practicing sports-medicine and laboratory experts, and benchmarked against the wearables the industry already trusts. Fitness-grade, and transparent about what we measure and how.*
  - CTA: `[Read the science →]` → Science
- **Layout:** centered, calm, authoritative.

#### Section 8 — Expert voices (quotes)  🟡
- **Intent:** Independent credibility via named advisor quotes.
- **Copy:**
  - Headline: **Backed by people who do this for a living.**
  - Quote 1 — *[DRAFT, get sign-off]* "…" — **[Advisor name], Head of Cardiovascology, a leading Belgrade hospital**
  - Quote 2 — *[DRAFT, get sign-off]* "…" — **[Advisor name], Head of Laboratory, Acıbadem Belgrade**
  - (NOT the investor/Head of Performance — background only.)
- **Assets:** advisor headshots + final approved quotes.

#### Section 9 — Final CTA band  🟡
- **Intent:** Close on the demo.
- **Copy:**
  - Headline: **See it on your squad.**
  - Sub: *Book a demo and we'll show you exactly what Hyvia surfaces for your athletes.*
  - CTA: `[Book a demo]`
- **Footer:** logo · nav (Platform · Solutions · Science · Company) · contact · `[Log in →]` · socials · legal.

- **SEO (Home):** Title — *Hyvia — AI readiness & performance monitoring for elite athletes* · Meta — *Continuous vitals and sweat-based markers like cortisol, turned into an AI readiness and performance forecast for every athlete. One coach dashboard.*

### 🟡 Platform — *the demoted "how." Keep short & functional; never upstage the outputs.*

#### Hero  🟡
- Headline: **One platform, from the body to the bench.**
- Sub: *Hyvia captures each athlete continuously, turns the data into clear scores, and puts them in front of the coach — automatically.*
- CTA: `[Book a demo]`

#### Data flow (diagram)  🟡
- **Capture** → the band and sweat patch read vitals and biomarkers continuously.
- **Analyze** → AI weighs each athlete's data against their own history.
- **Deliver** → scores and forecasts land in the coach dashboard and player app.

#### The parts (functional, not spec-sheet)  🟡
1. **Hyvia band** — continuous vitals: *heart rate, heart rate variability, blood pressure, oxygen, skin temperature.* Worn continuously, on and off the pitch.
2. **Sweat patch** — reads *cortisol, lactate and pH* from sweat. (generic "sweat patch" only — no tech/supplier detail)
3. **Coach dashboard** — every output, for the whole squad and each player.
4. **Player app** — each athlete's own data, readiness and history.

#### Always on, no extra work  🟡
- Headline: **Always on, no extra work.**
- Body: *Hyvia runs in the background — data flows automatically from the band and patch to the dashboard. No manual logging for athletes, no spreadsheets for staff.*

#### Data & privacy  🟡
- Headline: **Your data, your control.**
- Body: *Hyvia is GDPR-compliant. The club owns its athletes' data — always. We store and manage it securely on our own infrastructure, and the club can export or delete it at any time.*

#### Final CTA  🟡
- Headline: **See the platform in action.** → `[Book a demo]`

- **SEO:** Title — *Hyvia Platform — continuous wearable + sweat monitoring for teams* · Meta — *The Hyvia band and sweat patch capture vitals and biomarkers continuously; AI turns them into coach-ready scores in one dashboard. GDPR-compliant, club-owned data.*

### 🟡 Solutions — *the star page. Frame = coach's questions (Option B).*

**Page rules:** explain what each score *means*, NEVER how it's computed (no parameters). **Stress block must NOT mention cortisol/lactate.** Order follows the athlete's daily cycle.

#### Hero  🟡
- Headline: **Better calls, backed by the whole athlete.**
- Sub: *Hyvia turns continuous monitoring into clear answers to the questions coaches ask every day — for every player, every session.*
- CTA: `[Book a demo]`

#### Output blocks (question → output)  🟡
*Order = morning/recovery cluster → strain cluster → result/forecast cluster.*

1. **Readiness** — *"Who's recovered and ready to train?"*  ← lead output
   *Checked each morning before the session: how well each player has recovered from the day before, and how ready they are to train. One clear read on who's primed to push and who to hold back.*
2. **Sleep** — *"How well did each player sleep last night?"*
   *A clear picture of each athlete's sleep — naps included — quality, not just hours in bed.*
3. **Overload** — *"How much did today take out of each player?"*
   *The acute strain of a single day — how drained a player is after training and everything around it, measured against their own normal. Spot who took on more than usual, the day it happens.*
4. **Stress** — *"Who's under real physical and mental stress?"*
   *A combined read on physical and mental stress — the strain a player carries, whether it comes from training, pressure, or life off the pitch. The signal that separates a tough day from the road to burnout.* (❌ no "drained"; ❌ no cortisol/lactate mention)
5. **Fatigue** — *"Who's wearing down over time?"*
   *Where overload is one day, fatigue is the trend — chronic strain built up over recent days. Catch it before it turns into injury or a drop in form.*
6. **Performance score** — *"How did each player actually perform?"*
   *A performance score for every training session — an objective read on how each athlete performed, so coaches can compare, track progress, and reward the work that counts.*
7. **Performance prediction (AI)** — *"How will they perform next?"*  ← headline feature
   *Hyvia's AI learns each athlete from months of continuous data and projects how they're trending — so coaches can plan around who's rising, who's dipping, and who needs managing before it matters.*

#### Squad view  🟡
- Headline: **See your whole squad at a glance.**
- Body: *Every score, every player, in one dashboard — sort the squad by readiness, flag who needs attention, and drill into any athlete in a tap.*

#### Final CTA  🟡
- Headline: **See your squad through Hyvia.** → `[Book a demo]`

- **SEO:** Title — *Hyvia Solutions — readiness, stress, fatigue & performance for every athlete* · Meta — *Sleep, readiness, overload, stress, fatigue, per-session performance scores, and AI performance prediction — the coach-facing outputs Hyvia delivers for every player.*

### 🟡 Science — *leaner than usual. Stands on the honest stance + the expert panel.*

**Page rules:** NO algorithms/parameters. NO accuracy numbers. NO supplier names. Physiology stays **light** (no cortisol/lactate explainers). Citations = **founder-supplied later, never fabricated.**

#### Hero  🟡
- Headline: **Grounded in science. Honest about what that means.**
- Sub: *Hyvia is built with practicing sports-medicine and laboratory experts, and benchmarked against the wearables the field already trusts.*

#### Our approach (light, no formulas)  🟡
- Headline: **How Hyvia reads an athlete.**
- Body: *Hyvia combines continuous vitals and sweat biomarkers, and reads each athlete against their own baseline over time — so every score reflects that individual, not a population average. Grounded in established physiology, built for the real world.*

#### Fitness-grade, and honest about it  🟡
- Headline: **Fitness-grade — the right standard for daily monitoring.**
- Body: *Like the wearables your athletes already trust, Hyvia is fitness-grade — built for continuous, real-world monitoring, not clinical diagnosis. We're transparent about it: Hyvia surfaces trends and flags to support your decisions; it doesn't replace medical assessment.*

#### Built with experts (the panel)  🟡
- Headline: **Built with people who know the body.**
- **[Advisor name]** — Head of Cardiovascology, a leading Belgrade hospital — *cardiovascular & physical-stress expertise.*
- **[Advisor name]** — Head of Laboratory, Acıbadem Belgrade — *sweat-biomarker & biochemistry expertise.*
- **[HoP name]** — Head of Performance, a top-division football club — *applied performance; heart-rate, HRV & blood-pressure monitoring in elite sport.* (credential, NOT a testimonial)
- **Assets:** three headshots + titles. (Quotes stay on Home, advisors only.)

#### Research (DEFERRED to v1.1)  ⚪
- Slot for **third-party published research** on HRV / cortisol / lactate in sport. ❌ Do NOT fabricate. Add when founder supplies specific sources.

#### Final CTA  🟡
- Headline: **See the platform behind the science.** → `[Book a demo]`

- **SEO:** Title — *Hyvia Science — the approach behind the scores* · Meta — *Hyvia combines continuous vitals and sweat biomarkers, read against each athlete's own baseline — fitness-grade, built with sports-medicine and laboratory experts.*

### 🟡 Company — *the "who's behind this?" page. Curated leadership + science only.*

#### Hero / Mission  🟡
- Headline: **Performance has a blind spot. We built Hyvia to close it.**
- Sub: *Elite sport measures everything about an athlete's body — and almost nothing about the stress and chemistry that decide whether they peak or break. Hyvia gives every team a complete, continuous, forward-looking read on their athletes — body and mind.*

#### The story  🟡
- Headline: **Why we started Hyvia.**
- Body: *[Founder to refine — the founding insight: the cortisol / mental-stress gap in elite sport, and the vision to close it. 2–3 short paragraphs.]*

#### Leadership & science (curated — credibility only)  🟡
- Headline: **The people behind Hyvia.**
- **[CEO name]** — Founder & CEO — *serial entrepreneur; [1-line background].*
- **[Scientist name]** — [role] — *[expertise].*
- **[Biosensor scientist name]** — [role] — *wearable biosensor / biochemistry scientist.* (⚠️ generic description — do NOT say "microfluidic/electrosensor")
- ⛔ Operational/junior roles omitted by design.
- **Assets:** headshots + 1-line bios. Founder to supply names/roles.

#### Advisors  🟡
- Headline: **Backed by leading experts.**
- The 3-person panel (same as Science): 2 medical advisors + Head of Performance — credentials only.

#### Final CTA  🟡
- Headline: **Want to see what Hyvia can do for your team?** → `[Book a demo]`

- **SEO:** Title — *About Hyvia — the team building complete athlete monitoring* · Meta — *Hyvia gives elite teams a complete, continuous, forward-looking read on their athletes — body and mind. Meet the team and the science behind it.*

---

## 4. Founder to-do (content you must supply)
- [ ] Two **advisor quotes** (Home §8) + sign-off + headshots
- [ ] **Exact output names** confirmed vs. dashboard (Solutions)
- [ ] **Injury stat** citation (Home §3) — or it stays cut
- [ ] **Team names/roles/bios + headshots** (CEO, scientists, biosensor scientist)
- [ ] **Founding story** copy (Company)
- [ ] **Published research** citations (Science) — for v1.1
- [ ] **Dashboard screenshots** (hero, Solutions, Platform)
- [ ] Confirm advisors consent to being named
