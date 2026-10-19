# COS · Weekly rollup #4 + audit · 2026-10-19

**Summary.** The live app kept moving this week, all through the operator's own sessions. The seats did nothing:
- Games were refilled on 10-18 and now run to **10-24**, so they go empty again after Saturday.
- Mics grew from 270 to 337.
- Published articles grew from 34 to 53. 24 of those come from the sports, celebrity, pop and trending desks.
- Every news desk run was written by hand in a Claude chat, so there's no API spend.

The live app's code is still **not in GitHub**, so the five seats remain locked out. CTO, CCO and CRO are still frozen on the 10-08 permission prompts. New this week: the operator's two 10-18 sessions built **venue pitch decks for producing live shows**. Those don't fit any of the three pillars (scope flag below). North star: 1 Setlist subscriber, unchanged.

## North star

- **Setlist subscribers: 1 active.** Source: Beehiiv publication stats, all time, read 2026-10-19. There's still no growth since the 10-02 test sign-up.
- **Week-2 return rate: not measurable.** Analytics on the live app is UNKNOWN, and the code needed to check is not available.

## Blockers

| # | Blocker | What moved since 10-12 (D1 reads 2026-10-19 unless noted) |
| --- | --- | --- |
| 1 | Live app's code not in GitHub | **Nothing.** `list_repos` shows Hecklev2 and brax only. Asked on 10-08 and 10-12. |
| 2 | Games refill | **Partly.** A manual load on 10-18 13:48 UTC extended all 8 games to **10-24**. It's still manual and weekly, so it breaks the moment one week is missed. |
| 3 | Mic data trust | **Grew without review.** Live mics went from 270 to 337 (newest confirm 10-18). Mics confirmed more than 30 days ago went from 6 to **28**. The gathering method for the Instagram/Facebook-linked listings is still UNKNOWN. |
| 4 | Measurement | Nothing. |
| 5 | Festival fees, specials | 39 specials entries in D1. Not reviewed. |

## Rollup: shipped / blocked / next

| Seat | Shipped | Blocked on | Next |
| --- | --- | --- | --- |
| CTO | Nothing (3rd week) | Permission prompt since 10-08; no access to the live code | Refill automation, specials page spec |
| CAO | Nothing | Operator answers; the live code | Setlist |
| CCO | Nothing | Permission prompt since 10-08 | Fact-check live articles |
| CPO | Nothing | Operator answers | Games spec, mic audit |
| CRO | Nothing | Permission prompt since 10-08 | — |
| Operator sessions (outside the charter) | Games refill, 67 mics, 19 articles, 2 venue pitch decks | — | — |

## Audit (protocol §4)

- **Ran:** no seat ran since 10-01. All five *Last run* dates are 18 days old.
- **Rules:**
  - No seat produced anything, so no seat broke a rule.
  - The live content comes from operator sessions that **no seat reviews**: 19 new articles, 67 new mics, and 28 mics past 30 days still showing as live.
  - Under the universal rule "a wrong mic listing wastes their night", stale mics are the highest-risk item on the site.
- **Communication:** open inbox items older than 7 days:
  - CTO 5 (10-01 ×4, 10-08 ×1)
  - CCO 1 (10-01)
  - CAO 1 (10-02)
  - CPO 0
- **Drift / scope:**
  - **General news:** 24 of 53 published articles are sports, celebrity, pop or trending. This was raised on 10-12; no decision yet.
  - **Fourth business:** on 10-18 the operator's sessions built pitch decks to venues for Heckle-run live shows: "Comedy Mission: Pitch for Hyena's", and "Closed Session — Friday Comedy at The Cloak Room". Producing live shows is none of READ / TOOLS / PLAY. If these belong to Brax Productions (a separate business), they're outside Heckle and fine. If they're Heckle, **that's a fourth business. COS recommends parking it** until the five blockers move. Either way the operator decides; COS only flags it.
- **Verdicts:**
  - CTO: **Off track** (3 weeks, nothing, frozen)
  - CAO: **Off track** (no output)
  - CCO: **Off track** (frozen)
  - CPO: **Off track** (no output)
  - CRO: Needs attention (frozen)

  The cause isn't the seats. They're locked out of the live app and waiting on clicks. The fix is the two operator actions below.

## Weekly scan

- Nothing shipped this week that replaces a paid tool or a human job for us (searched 10-19).
- One free channel: **Listdle** ([listdle.com](https://listdle.com/)), a hand-curated directory of daily web games. A listing could bring players to Game Night for free. **WATCH**, handed to CAO, once the daily games and archive are reliable.

## Operator actions (in order, ~15 minutes)

1. **Push the live app's code to GitHub.** In the session that built it, ask it to push to a private repo and send me the link. This is the 3rd week of asking.
2. **Approve the 3 frozen prompts** in the CTO, CCO and CRO chats.
3. **Refill games before 10-24**, or let CTO automate it once #1 is done.
4. **Decide:** the news desks (keep, cut or review), and whether the venue pitches are Heckle or Brax.

## Unknown

- Analytics on the live app.
- How the Instagram/Facebook mics were gathered.
- Whether the venue pitches are Heckle or Brax.
