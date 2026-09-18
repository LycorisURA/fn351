# fn351

fn351 study guide platform — **The Coupon Strip**, a single-page study platform for Fixed Income Securities (A. Charoenrook).

Open `index.html` in a browser, or turn on GitHub Pages for this repo to host it.

## What's inside

- **Seven lecture coupons:** what a bond is, Treasury securities, arbitrage, term structure, pricing and returns, duration and convexity, interest rate futures.
- **Interactive tools**, including a quote desk, auction, repo, arbitrage bench, term structure, price–yield, SOFR futures desk, conversion factor, cheapest to deliver and futures hedge.
- **128 quiz questions**, each tiered easy / medium / difficult, with explanations. Every coupon can be **reattempted**, either one question at a time or the whole bank at once.
- **An endless drill**, generated on the page itself from 19 parametrised templates across all seven topics. Fresh numbers every time, so it never runs out and needs no network. Each template computes its own answer and builds its wrong options out of the mistakes people actually make on that question type — Macaulay where modified was wanted, ¼ instead of ½ on the convexity term, the annual coupon where the semiannual one belongs.
- **Assignments 1 and 2**, with hidden worked solutions.
- **Midterm prep:** rules, the lecturer's examples worked in full, and a mock exam in the 50 / 25 / 25 mix.
- **Textbook depth** from Fabozzi (ch. 1–6, 29) and Tuckman & Serrat (ch. 1–4), restated, with slide and manual errata flagged on the page.

## Design

The page runs on a **Nocturne Bazaar** palette — warm parchment and deep plum ink, with iris, jade, saffron, coral and sakura doing the semantic work. Light and dark are both first-class; the toggle sits in the masthead and is remembered.

## The desk calculator

Launched from the masthead or with **Alt+C**, closed with **Escape**, draggable by its title bar, and operable end to end from the keyboard. Three modes:

- **Expression** — a real recursive-descent parser rather than `eval`, so it works under a strict CSP and rejects malformed input with a readable reason instead of a silent `NaN`. Arithmetic, `^`, brackets, `sqrt ln log exp abs`, trig, `min max round`, `pi`, `e`, `ans` for the previous result, and a trailing `%` that divides by 100. Keeps a clickable tape of recent lines.
- **TVM** — N, I/Y, PV, PMT, FV, P/Y and a BGN switch, solving for whichever you leave out, on the same sign convention and key names as the financial calculator the exam requires. Closed form where one exists, bracketed bisection for N and I/Y.
- **Cash flows** — CF0 onward with repeat counts, giving NPV at a rate you choose and the IRR.

## The game layer

- **XP and levels.** 15 / 20 / 30 XP per correct easy / medium / difficult answer, 10 per tool you try, 50 per coupon clipped, 5 per Arbitrage Hunter win. Nine levels, each with a rank from Runner up to Rate Sovereign. XP is derived from saved progress, so it can never double-count.
- **Daily contracts.** Three objectives drawn from a pool each day, stable until midnight, worth 25–70 XP apiece.
- **No farming.** XP is derived from saved progress rather than accumulated, so reattempting a coupon gives the XP back before you re-earn it, and drill XP is capped.
- **Trophy case.** Sixteen achievements covering streaks, hard-tier answers, tools, mock scores, day streaks and a couple you'll have to find.
- **Mastery rings** on each coupon in the rail, filling as you answer its bank correctly. A coupon clips at 80%.
- **Streaks**, both answer streaks and consecutive-day study streaks.

## The companion

There is a study companion on this page. She is **off by default** — no card, no chat, no reactions, and the page never even asks for chat permission until she is woken. Waking her is a secret the page's owner knows; doing it again puts her back in the margin.

Once she is awake she has an **affection gauge** that rises as you study with her and cools if you leave her alone for days. It runs through six tiers, and her dialogue, faces and mood change at each one — she also reacts to headpats, trophies, contracts, level-ups, long sessions, tab-switching, text you highlight, and the numbers in every tool.

Note that this is a single static HTML file, so the secret is obfuscation rather than security: anyone reading the source can find it. What it guarantees is that the *default* experience carries no trace of her.

## Notes

- Progress is saved in your browser (localStorage), and synced to the artifact when the page runs as a published Claude artifact.
- The companion's chat only works when the page runs as a published Claude artifact. Everything else works anywhere.
