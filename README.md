# V2 Jets — "The Skies Are The Limit" · cinematic scroll-film site

A premium, scroll-driven cinematic website built for **V2 Jets**, a dedicated private-jet
charter specialist (founded 2015, Boca Raton, FL). This is a proposed site / design build for
the firm. It runs on a reusable scroll-film **engine** (`engine.js` / `engine.css` / `page.js` /
`serve.py`, copied verbatim, never edited) with a **skin authored from scratch** to a
"flight-deck atelier" art direction.

## Design world
A luxury private-aviation house where the night sky is the showroom and the UI is a calm,
exacting flight-deck interface. Single continuous **obsidian night** end to end (no light
sections). Cold **platinum** hairlines; a single **signal-cyan** live accent reserved for
active/live states; **brushed champagne** reserved for membership-tier markers only.

- **Type:** Playfair Display (display, tracked-tight uppercase) · Hanken Grotesk (body) · Space Mono (labels/mono).
- **Signature accent:** the **instrument readout** — a platinum hairline bracket framing a
  wide-tracked mono micro-label whose segment lights signal-cyan on view. Secondary: a drawn
  platinum flight-path hairline threading the chapters, and the V→2 chevron as bullet/divider.
- **Section order:** hero → manifesto → on-demand charter → fleet instrument strip →
  membership boarding-passes → growth/proof → closing CTA.

## Pages
- `index.html` — 7 film chapters + data sections + footer
- `fleet.html` — full fleet: cabin categories + the aircraft V2 operates across
- `membership.html` — Obsidian Membership + V2 Vault
- `staff.html` — Aviation Advisors (leadership + advisor bench)
- `reviews.html` — Client Voice (verbatim, sourced statements — no fabricated reviews)
- `contact.html` — request a flight, three offices, all contact actions wired

## Film chapters (frame sequences)
Seven scroll-scrubbed chapters, each a native-fps frame sequence under `assets/frames/<seq>/`:
`hero-ascent` · `cabin-altitude` · `fbo-dawn` · `fleet-tarmac` · `vault-route` ·
`global-reach` · `wheels-up-cta` — **192 frames each** (Veo 3.1, `quality:"ultra"`, 8s clips,
extracted at native fps). Each chapter's `data-count` in `index.html` is set to its frame count.

### Regenerating / re-extracting footage
Veo job IDs are in `jobmap.txt`. To re-pull a clip and re-extract frames:

```
sh extract.sh <seq> <rawUrl>      # downloads the clip → assets/frames/<seq>/%04d.jpg
```

`extract-all.sh` re-runs all seven at once. ffmpeg is bundled at `bin/ffmpeg`. After extraction,
set each chapter's `data-count` to the printed frame count in `index.html`.

## Run locally
```
python3 serve.py 8911
# open http://localhost:8911/
```

## Accuracy & sourcing
Every fact, name, stat, and quote is verified against public sources:
- Founded 2015; co-founders **Guy Endzweig** (Founder) & **Steven Rosenzweig** (Co-Founder);
  HQ Boca Raton, FL. Offices: Boca Raton, New York, Palm Beach (addresses per v2jets.com/contact).
  Phone 212-204-8422; info@v2jets.com.
- **Corporate Aviation acquisition** announced **early June 2026** (sources differ on the exact
  day — June 1 per PR Newswire, June 3 per Corporate Jet Investor; founded 2020; Bedford, MA &
  Fort Lauderdale, FL).
- Cabin categories, Obsidian jet card terms (25/50-hr blocks, fixed rates, no taxi time,
  72-hr non-peak callout, penalty-free cancellation, Caribbean & Canada coverage), and brand
  voice quoted verbatim from V2 Jets.
- **Attributed third-party figures:** the "$100M in annual sales" and V2 Vault **$100K / $250K**
  deposit are attributed to **Private Jet Card Comparisons** (not stated as V2's own claims). The
  $7,900/hr figure was omitted (shown as "quote on request") as it was not in primary sources.
- The legal disclaimer is kept **verbatim** in every footer:
  *"V2 Jets, LLC is an Air Charter Broker and not a U.S. or foreign direct air carrier in
  operational control of aircraft."*

## Notes on the build
The cinematic chapter footage is **AI-generated** (Veo 3.1) and treated to the brand grade; the
real V2 Jets logo and the firm's own photography are used in the flat data sections. Quoted
statements throughout are attributed to their public sources, and no client reviews are
fabricated. The fleet, membership, and contact details reflect V2 Jets' published information.
