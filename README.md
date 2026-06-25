# Tt tandtekniker — Webbplats

En komplett ombyggd, enksidig webbplats för **Tt tandtekniker**, ett tandtekniskt
laboratorium i Stockholm (tre generationer). Designkonceptet heter *"The Ceramist's
Atelier"* — ett ljust, galleriliknande uttryck i porslin och petrol som presenterar
tandtekniskt arbete som dyrbara objekt i en vitrin.

## Innehåll

```
tt-tandtekniker/
├── index.html              # Hela webbplatsen (HTML + CSS + JS i en fil)
├── robots.txt
├── sitemap.xml
└── assets/
    ├── images/             # Hero-/macrobilder, logotyp, 25 verkliga arbeten (work-01..25)
    ├── video/              # atelier-loop.mp4
    └── documents/          # arbetsorder.pdf (orderblankett)
```

## Publicera (deploy)

Webbplatsen är helt statisk — inga byggsteg, inga beroenden att installera.

- **Snabbast:** dra hela mappen `tt-tandtekniker/` till Netlify Drop, Vercel eller
  Cloudflare Pages.
- **Egen server / webbhotell:** ladda upp hela mappen så att `index.html` ligger i roten.
- **Testa lokalt:**
  ```bash
  cd tt-tandtekniker
  python3 -m http.server 8000
  # öppna http://localhost:8000
  ```

> Byt `https://tt-tandtekniker.se/` i `sitemap.xml`, `robots.txt` och `<link rel="canonical">`
> samt Open Graph-taggar om en annan domän används.

## Designsystem

- **Färger:** porslin `#F2F1ED`, ben `#FBFAF7`, bläck `#1A1814`, petrol `#123F39`.
- **Typografi:** Fraunces (display-serif), Hanken Grotesk (brödtext), IBM Plex Mono
  (teknisk data) — laddas via Google Fonts.
- **Signatur:** interaktiv VITA-nyansskala (B1–A4) och vitrin-/ljusmotiv.
- **Rörelse:** egen vanilla-JS (IntersectionObserver), respekterar `prefers-reduced-motion`.

## Funktioner

- Fast navigering med mobilmeny, mjuk scroll till sektioner.
- Interaktiv nyansskala, galleri med "Ladda fler", offert-/kontaktformulär som öppnar
  e-postklienten (mailto till `info@tt-tandtekniker.se`).
- SEO: titel/beskrivning, Open Graph, Schema.org `Dentist` med adress, telefon och
  öppettider. Responsiv från mobil till desktop.

## Innehåll som kan uppdateras

- **Bilder:** byt filer i `assets/images/` (behåll filnamnen, eller uppdatera `src` i
  `index.html`).
- **Texter, telefon, adress, omdömen:** redigeras direkt i `index.html`.
