# COS · Weekly rollup #2 + audit · 2026-10-05

**Summary.** Nothing has moved since 2026-10-01. No seat has run, no PR has merged, no deploy
has run, and the operator hasn't answered in the Immediate questions channel (checked
2026-10-05). The site is still not live. It's one settings toggle away: GitHub Pages is off, so
all 3 deploys failed. **Correction to rollup #1:** PR #8 ("Real data only", merged 2026-10-01
20:14 UTC) had already removed the fake mic confirm badges and the "41M views" figure. My
2026-10-02 rollup and interrupt said they were still live. They weren't. The error came from
writing from memory without pulling `main`. I sent a correction to the Immediate questions
channel today and fixed `memory/shared.md`. The bottleneck is the operator, not the seats:
about 21 open questions, plus 2 settings changes (Pages, network access) that block 3 seats.

## North star

- **Setlist subscribers: 1 active.** Source: Beehiiv publication stats, all time, read
  2026-10-05 ~07:50 US Central. Unchanged since 2026-10-02. The source is "website: direct" and
  the site isn't live, so it's most likely a test sign-up.
- **Week-2 return rate on games: not measurable.** It needs the site live, GA4 returning-user
  data, and 14 days of traffic. The earliest possible read is 14 days after Pages is switched on.

## Blockers, ranked

| # | Blocker | Owner | What moved since 2026-10-02 |
| --- | --- | --- | --- |
| 1 | Go live and measure | Operator (Pages setting), CTO (verify) | Nothing. Deploy run #3 (PR #8, 2026-10-01) also failed with the Pages 404, and no run since. Re-sent to Immediate questions 2026-10-05, with nothing to merge first. |
| 2 | Open mic feed | CTO, CPO | Nothing. Since PR #8 the page shows no generated mics, only sourced entries, and there aren't any yet. Operator cut it to 5 cities (CPO, 10-01); which 5 is undecided. |
| 3 | Backend | CTO | Nothing. CTO is waiting on 6 operator answers. Sign-up/mic notifications depend on it. |
| 4 | Festival fees and pay terms | CPO | Nothing. 0 of 8 verified, because the environment's network blocks the festival sites (CPO, 10-01). |
| 5 | Specials scores | CCO, CTO | Nothing. Since PR #8 every special shows "Not rated". Rubric v1 is done, and the CTO ledger spec isn't started. |

The order stands. Every blocker except #5 waits on an operator action; #5 waits on CTO.

## Rollup: shipped / blocked / next

| Seat | Shipped (all time) | Blocked on | Next |
| --- | --- | --- | --- |
| CTO | Survey of browser-storage surfaces (memory only, no report) | 6 operator questions | 6 inbox asks: sign-up block, notifications path, mic evidence fields, score ledger, go-live verify |
| CAO | [5 Setlist drafts + sign-up audit](../cao/2026-10-01-setlist-drafts-and-signup-audit.md) | Operator: launch cities, where drafts live, network access | Beehiiv rename checklist (inbox) |
| CCO | [Scoring rubric v1](../cco/2026-10-01-scoring-rubric.md) | Operator: hand-entered RT scores OK? | Set/Bomb of the Week selection rule (inbox) |
| CPO | [Mics + festivals plan](../cpo/2026-10-01-mics-festivals-plan.md) | Operator: 5 cities, IG/FB rule, network access | Festival check once the network allows it |
| CRO | [7 questions](../cro/2026-10-01-first-assignment-questions.md) | Operator: all 7 | Smallest honest 60-day sale |
| COS | Escalation rule, rollups #1–#2 | Operator: build hours | Rollup #3, 2026-10-12 |

## Operator ship list (in order, about 1 hour total)

1. **Turn on Pages** (Settings → Pages → Source: GitHub Actions) and re-run "Deploy site". This unblocks #1 and starts the north-star clock.
2. **Allow network domains** for the seats' cloud environment: environment settings → Network
   access → Custom, adding the festival sites CPO listed plus Eventbrite. Steps:
   https://code.claude.com/docs/en/cloud-environments#network-access. This unblocks #4 and CAO's checks.
3. **Pick the 5 mic cities.** It unblocks #2, CAO's newsletter mic item, and CPO.
4. **Answer CTO's 6 questions.** That seat has the most queued work.

## Audit (protocol §4)

- **Ran:** none of the five seats ran between 2026-10-02 and 2026-10-05. That isn't a failure,
  because all are blocked on the operator. Each *Last run* is 2026-10-01 and accurate.
- **Rules:** no breaks. Two figures came close, and both were handled correctly:
  - CPO: "$29–$49, closing 2026-06-30" from a search summary, marked "**NOT verified** and is not recorded as a fee" ([report](../cpo/2026-10-01-mics-festivals-plan.md), line 17).
  - CCO: RT licence "from $60,000/yr", marked "third-party, unconfirmed" with links ([report](../cco/2026-10-01-scoring-rubric.md), line 121).

  COS broke rule 6 in spirit. Rollup #1 stated that two leaks were live without re-checking
  `main`. Corrected above. New COS rule: `git pull` before any claim about site state.
- **Communication:** 8 open inbox items. None is older than 7 days; the oldest is from
  2026-10-01, 4 days ago. All went to the right seat. Two are now **stale**:
  - CPO → CTO, "label sample mic badges" (10-01): done by PR #8. CTO should tick it.
  - COS → CTO (10-02): the "treat the sample-badge PR as pre-launch" half is moot; the go-live verify half stands.

  CCO memory still lists "41M views" as an open item; PR #8 removed it.
- **Drift:** none toward general comedy news. One **sustainability flag**: CAO's Setlist plan is
  *daily* at 7 a.m. (operator format, 10-01). Under universal constraint #2, a daily send only
  works while the operator approves an issue every morning. On a week they're away, it stops.
  CAO should propose the version that survives an absent week, such as queued drafts or a
  weekly fallback. That's a CAO call, so it's handed off.
- **IG/FB:** CPO asked the operator to keep or "knowingly override" the no-scraping rule for
  Instagram/Facebook. COS position: an override is a legal risk (Meta's terms), so it would go
  through the escalation channel, not a rollup. Recommend keeping the rule.
- **Verdicts**
  - CTO: **Needs attention.** 6 open inbox items and no report yet. It's blocked by the operator, but it's the busiest queue on the team.
  - CAO: On track.
  - CCO: On track. Its memory is stale on one item.
  - CPO: On track.
  - CRO: On track. It's fully blocked, and correctly so.

## Weekly scan

1. **beehiiv new plans and pricing, effective October 2026.** WHAT: tiers renamed to Free / Lite /
   Pro / Enterprise; reported price rises up to 52% on paid tiers; API and MCP access promoted
   ([beehiiv blog](https://www.beehiiv.com/blog/beehiiv-pricing-2026),
   [WERSM](https://wersm.com/beehiiv-raises-prices-creator-business/), seen 2026-10-05 via search,
   not read in full). WHY US: The Setlist runs on beehiiv. We're on the Free plan as far as COS
   knows (UNKNOWN, not checked). The Free plan's subscriber cap and features under the new plans
   are UNKNOWN. **WATCH.** CAO to confirm the Free plan's limits on beehiiv's own pricing page
   before any paid plan is considered.
2. **beehiiv MCP.** WHAT: beehiiv tools that pull stats and draft posts; this session used them
   today, read-only. WHY US: CAO could save Setlist drafts in beehiiv unsent and read open rates
   without a human, at no added cost. **KEEP** for reads. Drafting is CAO's call and needs the
   operator's OK on "Beehiiv drafts vs repo".
3. **GitHub Actions retention change (2026-10-01).** WHAT: run and check history now follows the
   artifact retention setting ([changelog](https://github.blog/changelog/2026-10-01-actions-retention-now-covers-checks-runs-and-statuses/)).
   WHY US: barely relevant; old deploy logs may expire. **SKIP.**

Not reported: static-site form backends with free tiers turned up in search, but none
shipped this week. CTO already owns that question.

## Unknown

- The Pages setting right now: UNKNOWN. COS can't read repo settings; the last deploy evidence is from 2026-10-01.
- Whether the 1 subscriber is a real person: UNKNOWN. COS didn't open the private subscriber list.
- The operator's build hours: UNKNOWN (asked 2026-10-02).

## What COS is still missing

- An operator reply in the Immediate questions channel. Two messages there have no reply yet.
- A read-only way to see repo settings (Pages status).
- The build hours, to defend calendar time.
