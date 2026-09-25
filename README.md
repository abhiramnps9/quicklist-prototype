# QuickList — Campus Listing Board (Concept C10)

> Borrow, buy, sell or share anything on campus — one verified board, no app to install.

A fully working, single-file prototype built for the **Everyday Evolved** project, Concept **C10 — Lightweight Listing Board**. This repository contains the live, clickable prototype used to test the concept's feasibility, not a mockup or a set of static screens.

| | |
|---|---|
| **Student** | Surya Abhiram |
| **Roll No.** | CB.EN.U4ARE24031 |
| **Course** | 23ARE382 · Design Thinking |
| **Team** | Everyday Evolved |
| **Assignment** | Individual concept development — feasibility, bill of materials & virtual model |

---

## 1. Problem this solves

Useful items on campus — cycles, textbooks, tools, sports gear, project hardware — regularly sit idle with one student while another pays to rent or buy the same thing for a short-term need. Existing options (OLX, informal WhatsApp groups, Rentomojo) each cover only part of the problem: none combine renting, buying and selling in one place, none confirm the other party is actually a student, none capture proof of an item's condition, and none turn reliable lending into a visible reputation.

QuickList answers this with the simplest possible build: a single, verified listing board — deliberately without a bot, an app-store release, or an escrow system — to test whether verification, photo proof and a visible reliability score actually change borrowing behaviour before investing in anything heavier.

## 2. Core features

- **Simulated identity verification** — a college-email/OTP-verified banner appears before a listing can be posted, standing in for a one-time moderator ID check
- **Post a listing** — item name, category, exchange type (Rent / Borrow / Buy-Sell / Share), a short condition note, contact info, and an optional condition photo
- **Browse & filter** — a live search bar plus category chips (Cycles, Books, Sports Gear, Project Hardware, Tools, Mess Food, Other)
- **Reveal contact** — a manual "match & request" step; clicking a listing reveals the lister's phone number or room, handing the conversation off outside the app
- **Reliability score** — every lister can be rated 👍/👎 by others; the app calculates and displays a live reliability percentage on each of their listings
- **Mark as returned** — closes the loop on a rent/borrow listing once the item is back
- **Live counters** — header stats for live listings, verified students, and items returned on time

## 3. How it maps to the concept's workflow

| Step | What the prototype does |
|---|---|
| Verify | Shows a simulated "college email OTP verified" banner on the posting form |
| List | Captures category, exchange type, description and an optional photo |
| Discover | Search bar + category chips filter the board instantly |
| Request | "Reveal contact" button surfaces the lister's phone/room |
| Exchange | Agreed informally between the two students — no deposit, no in-app payment |
| Close & rate | "Mark returned" + a thumbs-up/down vote that updates the lister's reliability score |

## 4. Tech stack

Everything is intentionally free-tier and dependency-free, so it can be built and hosted at **zero cost**:

- **Frontend:** vanilla HTML, CSS and JavaScript — no framework, no build step, no npm install
- **Fonts:** Google Fonts (Fraunces + IBM Plex Sans), loaded via CDN `<link>` tags
- **Data storage:** browser `localStorage` — listings and reliability scores persist per browser/device, with no backend server or database
- **Hosting:** static hosting only (GitHub Pages, Netlify, or any static host)

Because it's a single self-contained `index.html`, there is nothing to install, build or configure — open the file (or the hosted link) and it works.

## 5. File structure

```
quicklist-prototype/
├── index.html     # the entire app — markup, styling and logic in one file
└── README.md      # this file
```

## 6. Running it locally

No installation needed:

1. Download `index.html`.
2. Double-click it, or open it in any modern browser (Chrome, Edge, Firefox, Safari).
3. That's it — sample listings load automatically.

## 7. Hosting it live (GitHub Pages)

1. Create a new **public** GitHub repository (e.g. `quicklist-prototype`).
2. Upload `index.html` and `README.md` to the repository root.
3. Go to **Settings → Pages**.
4. Under "Build and deployment," set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`, then **Save**.
5. After ~30–60 seconds, GitHub publishes the site at:
   `https://<your-username>.github.io/quicklist-prototype/`
6. That link is public and permanent — no login required to view it.

## 8. Known limitations (prototype scope)

These are intentional simplifications for a fast, zero-cost pilot, not oversights:

- **No real backend** — data lives in the visitor's own browser (`localStorage`), so listings don't sync across devices or reset if the browser cache is cleared.
- **Identity verification is simulated** — the "verified" banner is a placeholder for what would be a real one-time moderator/ID check in production.
- **No authentication** — anyone opening the page can post as anyone; a production version would need real login.
- **No payments or deposits** — by design, matching the concept's "reputation only, no deposit" approach.

## 9. Possible next steps

- Replace `localStorage` with a shared backend (e.g. Google Sheets + Apps Script, or Firebase free tier) so listings sync across everyone viewing the board
- Add real OTP-based college email verification
- Add push/email notifications when a listing's status changes

## 10. Credits

Built as part of the **Everyday Evolved** concept set for the Design Thinking course (23ARE382). Concept C10 was developed collaboratively by the team; this prototype and its accompanying feasibility report were built individually by Surya Abhiram.
