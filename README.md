# ⚡ NeuralPulse

> A free, open-source AI tools & trends hub for developers and students.

**Live site:** `https://yourusername.github.io/neuralpulse`

---

## What is NeuralPulse?

NeuralPulse is a lightweight, single-file web app that keeps you up to date with the latest AI tools, news, and trends. It's built for developers, students, and anyone who wants to stay ahead in the fast-moving AI space — without paying for anything.

---

## Features

- 🔴 **Live news ticker** — scrolling headlines pulled from real AI news sources
- 🔥 **Featured tool spotlight** — hand-picked tool of the week
- 🔍 **Search & filter** — browse 12+ curated AI tools by category (Writing, Coding, Image, Video, Audio, Research)
- 📰 **Daily news feed** — auto-fetches fresh articles from AI RSS feeds every day; cached so it never hammers the API
- 📈 **Trending sidebar** — top searches in AI this week
- ✉️ **Newsletter signup** — email capture with confirmation
- 📊 **Animated hero stats** — live-counting numbers on page load
- 🎨 **Premium dark UI** — editorial aesthetic with custom cursor, scroll progress bar, and smooth animations

---

## Tech Stack

| Layer | Technology | Cost |
|---|---|---|
| Frontend | HTML, CSS, JavaScript | Free |
| Hosting | GitHub Pages | Free |
| News data | RSS feeds via rss2json.com | Free |
| Fonts | Google Fonts | Free |

No frameworks. No build tools. No backend server. Just one `index.html` file.

---

## Getting Started

### Option 1 — Use it directly
Download `index.html`, open it in any browser. Works offline with fallback news data.

### Option 2 — Deploy to GitHub Pages (recommended)

1. Fork or clone this repo
2. Make sure the main file is named `index.html`
3. Go to **Settings → Pages**
4. Set source to **main branch / root**
5. Your site is live at `https://yourusername.github.io/neuralpulse`

---

## How the News Works

NeuralPulse fetches live AI news from multiple RSS sources on page load:

- VentureBeat AI
- The Verge — AI section
- The AI Report

Results are **cached in localStorage** by date, so the API is only called once per day. If all sources fail, a curated set of fallback articles with real links is shown instead.

To change the news sources, edit the `RSS_SOURCES` array in the script section of `index.html`.

---

## Customisation

Everything lives in a single `index.html` file. Here's what's easy to change:

**Add or edit tools** — find the `tools` array in the `<script>` section and add an object:
```js
{ name: "Tool Name", desc: "Short description.", cat: "coding", icon: "🤖", free: true, stars: 5, link: "https://example.com" }
```

**Change the featured cards** — edit the two `.featured-card` blocks in the HTML.

**Update the ticker** — edit the `.ticker-item` spans near the top of the `<body>`.

**Change colours** — edit the CSS variables at the top of the `<style>` block:
```css
:root {
  --accent: #00E5FF;   /* cyan */
  --accent2: #FF3CAC;  /* pink */
  --gold: #F0C040;     /* gold */
}
```

---

## Project Structure

```
index.html   ← entire app (HTML + CSS + JS in one file)
README.md    ← this file
```

---

## License

MIT — free to use, fork, and modify for personal or commercial projects.

---

Built with 0 dependencies and $0 in hosting costs.
