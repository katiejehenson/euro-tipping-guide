# 🌍 European Tipping Guide

A clean, interactive tipping reference for travellers visiting 8 European countries — covering restaurants, private transfers, tour guides, hotels, and more.

**Live site →** `https://<your-username>.github.io/<your-repo-name>/`

---

## Countries covered

| Country | Currency |
|---|---|
| 🇫🇷 France | EUR (€) |
| 🇮🇹 Italy | EUR (€) |
| 🇪🇸 Spain | EUR (€) |
| 🇩🇪 Germany | EUR (€) |
| 🇬🇧 United Kingdom | GBP (£) |
| 🇬🇷 Greece | EUR (€) |
| 🇵🇹 Portugal | EUR (€) |
| 🇳🇱 Netherlands | EUR (€) |

Each country includes guidance on:
- Restaurants & cafés
- Taxis & private transfers
- Tour guides (group & private)
- Hotels, housekeeping & concierge
- Country-specific categories (gondoliers, fado performers, boat captains, etc.)

Plus a **Universal Guide** with private transfer & guide benchmarks across all price points, and **6 etiquette tips** that apply everywhere in Europe.

---

## Tech stack

- Pure HTML + CSS + Vanilla JavaScript — **zero dependencies, no build step**
- [Raleway](https://fonts.google.com/specimen/Raleway) via Google Fonts
- Fully responsive, mobile-friendly
- Accessible (keyboard navigable, `aria` attributes on interactive elements)

---

## Deploy to GitHub Pages

### Option A — Upload the file directly

1. Create a new GitHub repository (public)
2. Upload `index.html` to the root of the repo
3. Go to **Settings → Pages**
4. Under *Source*, select **Deploy from a branch**, choose `main`, folder `/root`
5. Click **Save** — your site will be live at `https://<username>.github.io/<repo>/`

### Option B — Clone & push

```bash
git clone https://github.com/<username>/<repo>.git
cd <repo>
cp /path/to/index.html .
git add index.html
git commit -m "Add European tipping guide"
git push origin main
```

Then enable GitHub Pages in Settings as above.

---

## Customisation

All country data is defined in the `COUNTRIES` array inside the `<script>` block at the bottom of `index.html`. Each entry follows this shape:

```js
{
  name: "France",
  flag: "🇫🇷",
  currency: "EUR (€)",
  culture: "One-line cultural overview shown under the country name.",
  categories: [
    {
      icon: "🍽️",
      label: "Restaurants",
      tip: "Round up or leave €1–2",        // shown in the collapsed row
      detail: "Longer explanation shown when the row is expanded."
    },
    // …up to 8 categories
  ],
  note: "Italicised footer note about local tipping norms."
}
```

Colors are defined as CSS custom properties at the top of the `<style>` block:

```css
:root {
  --primary:   #3EE7C6;   /* turquoise — accents, buttons, borders */
  --secondary: #7CE9E5;   /* lighter turquoise — gradients          */
  --light:     #B1E9F3;   /* pale blue — subtle accents             */
  --navy:      #2B4A6F;   /* dark blue — page background            */
  --navy-dark: #1e3550;
  --navy-mid:  #243d5e;
  --navy-deep: #1a3050;
  --white:     #F0FAFE;
  --muted:     #7aafc8;
  --faint:     #3d6a8a;
}
```

---

## License

MIT — free to use, adapt, and redistribute.
