# Calendar Wallpaper

A live, interactive calendar wallpaper for the Mac desktop, rendered by
[Plash](https://github.com/sindresorhus/Plash). One self-contained `index.html`:
no build step, no dependencies, no tracking.

## What it shows

- The weekday and today's date as a large numeral
- The current month, year, and a mini month calendar with today marked
- A background palette chosen automatically from the month and season

## Settings

Hover the **bottom-right gear**, or **click the big date numeral**, to open the
panel. (The numeral works as a fallback when a menu bar or dock covers the gear.)

| Setting        | Options                    |
| -------------- | -------------------------- |
| Fill           | Gradient / Solid           |
| Hemisphere     | North / South (flips the season) |
| Week starts    | Sun / Mon                  |
| Layout         | Center / Corner            |

Choices are saved in `localStorage`, so they persist across reloads.

## The 12 palettes (Northern hemisphere)

| Month | Mood |
| --- | --- |
| January | deep winter — midnight blue → ice |
| February | late winter — frost & lavender |
| March | early spring — pale thaw green |
| April | spring — blossom pink |
| May | late spring — lush green |
| June | early summer — sky & gold |
| July | high summer — sun / coral |
| August | late summer — amber |
| September | early autumn — ochre |
| October | autumn — rust |
| November | late autumn — plum & bark |
| December | deep winter — pine |

Southern hemisphere shifts the palette by six months.
Edit the `PALETTES` array in `index.html` to retune any colour.

## Deploy to GitHub Pages

1. Create a repo (e.g. `calendar-wallpaper`) and push this folder.
2. Repo **Settings → Pages → Build and deployment → Source: Deploy from a branch**,
   branch `main`, folder `/ (root)`, Save.
3. Wait for the build; your page is at
   `https://<username>.github.io/calendar-wallpaper/`.

## Set up in Plash

1. Install **Plash** (free, Mac App Store).
2. Plash menu bar → **Add Website** → paste the GitHub Pages URL.
3. Recommended Plash settings:
   - **Reload Interval:** 1 hour (the page also refreshes itself at midnight)
   - **Bring Browser to Front / Browsing Mode:** enable when you want to click the
     gear and change settings, then turn it back off
4. Multiple displays: add the same URL per screen if desired.

To iterate locally without deploying, point Plash at the `index.html` file directly
(`file:///…/index.html`) — settings and palettes still work; only future Google
Calendar integration needs a real origin.
