# is it safe to bike?

A one-page placard that answers one question: if you leave Hack Club HQ on a
bike right now, are you going to get poured on?

Open `index.html` — it's the whole site, no build step, no dependencies. It
fetches the [Open-Meteo](https://open-meteo.com/) 15-minute forecast for
212 Battery St, Burlington VT and gives you one of three verdicts:

- **GO BIKE.** — under 0.6 mm/h for your whole ride; you won't notice it
- **YOU'LL GET DAMP.** — light rain (up to 2.6 mm/h); rideable, bring the jacket
- **NOPE. STAY IN.** — real rain or thunder; make some tea

Below the verdict: the next six hours of sky in 15-minute boxes (blue fill =
rain intensity, hatch = the sky is undecided), and when the next dry window
long enough for a ride opens up.

The black bar on top of the strip is your ride. **Drag its end** (or focus the
strip and use arrow keys) to match how long you'll be out — the verdict
recomputes as you drag, and the length is remembered in `localStorage`. At the
bottom, one quiet line answers the evening question: does the bike need its
cover on at home tonight (any hour with ≥0.5 mm in the next 18 hours).

## Tuning

Everything adjustable is a constant at the top of the script in `index.html`:
the office coordinates and timezone, the default ride length (45 min), and the
drizzle/pouring/cover thresholds.

## Hosting

It's a single static file — GitHub Pages on this repo works as-is, or drop it
anywhere that serves HTML.
