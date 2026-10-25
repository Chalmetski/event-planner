# Event Planner

Web-app om events met meerdere zalen te plannen: kalenderblokken per kwartier per zaal, een vast team per zaal en
live collega-beschikbaarheid (vrij/bezig). Delen via een link met de data erin.

## Stack
- Eén zelfstandig HTML-bestand, vanilla JS, geen build. Libs lokaal: `lz-string.min.js`, `qrcode.min.js`.
- Bluemoon-design (`C:\dev\design\DESIGN_SYSTEM.md`), light-first.

## Draaien
- `index.html` openen in de browser (Windows, Mac, iPhone, Android).
- Lokale server (staat in de gitignorede `.claude/launch.json`): `python -m http.server 5577`.
- Live: GitHub Pages, https://chalmetski.github.io/event-planner/ (repo public, branch `main`, root). Pushen naar `main` = publiceren.
- Geen tests.

## Structuur
- `index.html` — alles (state, rendering, modals, delen).
- `lz-string.min.js`, `qrcode.min.js` — vendored libs.

## Functies en domein
- Event met naam, datum en begin-/einduur; meerdere dagen via de dagbalk (elk blok hoort bij één dag, beschikbaarheid per dag).
- Zalen: naam + kleur (stalen of eigen `<input type=color>`); kleur = top-border + stip in de kop en gekleurde kolomrand.
- Rooster: verticale tijdas, kolommen = zalen, 15-min-slots. Sleep om een blok te maken; op desktop slepen/resizen om te bewerken.
- Blok-types standaard: Technische assistentie, Plaatsing, Demontage, Transport, Laden, Lossen + eigen types met kleur.
- Collega's met avatarkleur; vast team per zaal. Bij een blok toont de collega-lijst live Vrij / Bezig (welke zaal) /
  team van deze zaal op dat tijdstip (overlapdetectie via `busyBlock()`).
- Bewerken (slepen/resizen) hoeft niet op gsm te werken.

## Opslag en delen
- Auto-save naar localStorage, key `eventplanner.v1`.
- Hoofd-deelmethode = link met data: hele state → `LZString.compressToEncodedURIComponent` → `#p=...` in de URL
  (`encodeState`, `shareURL`). Bij opstart laadt `tryLoadFromHash()` een gedeelde link (met confirm als er lokaal werk is).
- Deel-venster: QR (qrcode-generator), WhatsApp-knop (wa.me), Kopieer, `navigator.share` op mobiel.
- JSON export/import blijft als alternatief.
- Een deel-link werkt voor anderen enkel vanaf de gehoste versie, niet vanaf `file://`.

## Valkuilen
- De repo is public (GitHub Pages): geen interne gegevens of echte planningen committen.
- De UI gebruikt nog emoji als iconen (o.a. 📅 🔗 👥 🗑 💾); de globale regel is line-icons.

## Open idee
- Live cloud-sync (gedeelde server) als delen via link niet volstaat. Geen Cloudflare (bedrijfsbeleid).
