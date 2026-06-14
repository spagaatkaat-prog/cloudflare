# 📝 Essaybundel Nakijker

Een mobielvriendelijke web-app om je essays mee na te kijken. Alles draait in je
browser: niets installeren, geen account, en je teksten blijven op je eigen toestel.

## Wat doet het?

**Directe controles (gratis, werkt zonder internet en zonder API-sleutel):**
- Essays inladen uit **.docx**- en **.txt**-bestanden (of gewoon plakken); meerdere
  tegelijk komen meteen in je bundel
- Woord-, zin- en alineatelling + geschatte leestijd
- Leesbaarheidsscore (Flesch-Douma, aangepast voor het Nederlands)
- Lange zinnen die je kunt opknippen
- Vaak herhaalde woorden en weinig woordvariatie
- Vul- en stopwoorden (eigenlijk, gewoon, heel, …) die je vaak kunt schrappen
- Vage/zwakke woorden, mogelijke clichés en lijdende vorm
- Dubbel getypte woorden
- Eén overzichtsscore per essay + een tabel over de hele bundel

**Optionele AI-feedback (inhoudelijk):**
- Stijl, structuur en sterke/zwakke punten, beoordeeld door Claude
- Gebruikt je eigen Anthropic API-sleutel, die **alleen in je browser** wordt bewaard
  en rechtstreeks naar Anthropic gaat (niet naar een tussenserver)

## Openen op je telefoon

1. Host de map online (zie hieronder) en open de link op je telefoon.
2. Tik in je browser op "Zet op beginscherm" / "Add to Home Screen" — dan opent
   het als een app.

## Online zetten (Cloudflare Pages)

Deze map bevat alleen statische bestanden, dus hosten is gratis en simpel:

1. Ga naar **Cloudflare Dashboard → Workers & Pages → Create → Pages**.
2. Koppel deze repository en kies deze map (`essay-nakijker`) als build-uitvoermap.
   Er is geen build-stap nodig (framework: *None*, output directory: `essay-nakijker`).
3. Deploy → je krijgt een `*.pages.dev`-link die je op je telefoon kunt openen.

Of test het meteen lokaal: download `index.html` en open het in je browser.

## Privacy

- Je essays worden opgeslagen in de lokale opslag van je browser (`localStorage`).
- Wis je de browsergegevens, dan ben je ze kwijt — exporteer af en toe een back-up
  via **Instellingen → Bundel exporteren**.
- De API-sleutel (als je AI-feedback gebruikt) staat alleen op je toestel.
