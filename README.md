# is it safe to bike?

A one-page placard that answers one question: if you leave Hack Club HQ on a
bike right now, are you going to get poured on?

Open `index.html` — it's the whole site, no build step, no dependencies. It
fetches the [Open-Meteo](https://open-meteo.com/) 15-minute forecast for
Shelburne VT and gives you one of three verdicts:

- **GO BIKE.** — under 0.6 mm/h for your whole ride; you won't notice it
- **YOU'LL GET DAMP.** — light rain (up to 2.6 mm/h); rideable, bring the jacket
- **NOPE. STAY IN.** — real rain or thunder; make some tea

Below the verdict: the next six hours of sky in 15-minute boxes (blue fill =
rain intensity, hatch = the sky is undecided), and when the next dry window
long enough for a ride opens up.

## Tuning

Everything adjustable is a constant at the top of the script in `index.html`:
the office coordinates and timezone, the ride length (45 min), and the
drizzle/pouring thresholds.

## Hosting

It's a single static file — GitHub Pages on this repo works as-is, or drop it
anywhere that serves HTML.
