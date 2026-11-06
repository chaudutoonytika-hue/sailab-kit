# Sailab Kit

An offline first-aid guide for floods, heatwaves and outages, when there is no signal and no time to search the web.

Built for [Hackyard Yard #6: Offline](https://hackyard.tech/yards/yard-6).

## What it does

- Step-by-step decision trees: tap what is happening, get the right steps.
- Topics: CPR and not breathing, snakebite, burns, heatstroke, severe bleeding.
- Instant search across every topic.
- One-tap emergency numbers: Rescue 1122, Edhi 115, Police 15.
- Large, high-contrast text with an A- / A+ control. Light and dark mode follow the device.

## Zero network, by design

- One `index.html`. No frameworks, no fonts, no images, no `fetch()`, no analytics.
- Works straight from disk: download `index.html` and open it in a browser with airplane mode on.
- When hosted over HTTPS, a small service worker (`sw.js`) caches the page so the installed site keeps working offline.

## Run it

```bash
git clone <this-repo>
cd sailab-kit
open index.html        # or double-click it
```

To host on GitHub Pages: Settings, Pages, deploy from the `main` branch, root folder.

## Airplane-mode test

1. Open the page once (or the file from disk).
2. Turn on airplane mode.
3. Reload. Search for "snake", walk through a topic. Everything still works. The badge in the header reads "Offline: still works".

## Editing content

All guidance lives in the `T` (topics) and `N` (nodes) objects at the top of the script in `index.html`. A node is either a question (`q`, with options `o`) or an instruction card (`h` heading, `d` steps, `a` things to avoid, `n` note, `g` extra links, `call` to show the call button).

## Medical disclaimer

This app gives general first-aid guidance written to match widely published advice from bodies such as the WHO, the Red Cross and national resuscitation councils. It is not a substitute for professional medical care or training. Call emergency services first whenever you can. Have a qualified clinician review the content before relying on it in real emergencies, and confirm local emergency numbers for your area.

## License

MIT
