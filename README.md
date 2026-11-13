# 🏔️ Missoula Happenings: missoula-activities

What's going on in Missoula, built for a University of Montana student and family: **UM campus, downtown, the rest of Missoula, Bonner/East Missoula (KettleHouse), Lolo/Bitterroot, Frenchtown and Seeley Lake**.

**Live site:** https://joemarcouxid.github.io/missoula-activities/

## What it does
- **Today · This Weekend · Next 7 Days · This Month · This Year** tabs, with a count on each
- **🎟 Plan Ahead**: concerts and big events a week or more out (KettleHouse Amphitheater, The Wilma, Top Hat, Adams Center, Washington-Grizzly Stadium, Dennison Theatre), with **🆕 newly announced** flags
- **UM Campus** filter: GrizHub student events, UM arts and culture, Griz home games
- **⭐ My List**, town and kind filters, search, **🔄 Refresh**, **📅 Add to calendar**, **＋ Add a tip**
- Times show in **Mountain time** (Missoula's local time), even when viewed from Washington

## Heads-up for tickets
1. **Phone calendar:** on the Plan Ahead tab tap **Subscribe on this phone** (`webcal://joemarcouxid.github.io/missoula-activities/data/plan-ahead.ics`).
2. **Email / GitHub app alert:** new concerts and big events open a "🎟 New events announced" issue. **Watch** this repo to get notified.

## How it works
Every 3 hours GitHub Actions runs `scripts/collect.py` over the sources in `docs/data/sources.json` (GrizHub, UM events, Griz athletics, Destination Missoula, Missoula Downtown Partnership, Missoula Public Library, Logjam Presents, ZACC, Songkick, AllEvents, HappeningNext, r/missoula, r/umt and Bluesky), tags events by area using `docs/data/region.json`, and writes `docs/data/events.json`. GitHub Pages serves `docs/`.

Same engine as [wenatchee-activities](https://github.com/joemarcouxid/wenatchee-activities) and [spokane-activities](https://github.com/joemarcouxid/spokane-activities); only `docs/data/region.json` and `docs/data/sources.json` differ.
