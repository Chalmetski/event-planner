# Event Planner

Eén-bestand web-app om events met meerdere zalen te plannen. Opent op **Windows, Mac, iPhone en Android** in elke browser — geen installatie nodig.

## Openen
Dubbelklik op `index.html` (of sleep het naar je browser). Op telefoon: stuur het bestand naar jezelf en open het, of host het ergens (zie onderaan).

## Wat kan je?
- **Zalen toevoegen** — knop `＋ Zaal` rechts bovenaan het rooster. Klik `⋯` bij een zaal om de **naam en kleur** te wijzigen (kies uit stalen of een eigen kleur).
- **Blokken plannen** — sleep in een zaalkolom van begintijd tot eindtijd (per kwartier). Er opent een venster om type, omschrijving, tijd en collega's te kiezen.
- **Collega's per zaal** — klik het 👥-icoontje bij een zaalnaam om een vast team toe te wijzen.
- **Zien wie vrij is** — bij het toevoegen van een blok toont de collega-lijst meteen wie *Vrij*, wie *Bezig* (en in welke zaal) en wie *team van deze zaal* is, op dat exacte tijdstip.
- **Blok-types** — standaard: Technische assistentie, Plaatsing, Demontage, Transport. Eigen types toevoegen via `🏷️ Blok-types`.
- **Aanpassen** (op desktop) — klik een blok om te bewerken, sleep het om te verplaatsen, sleep de boven-/onderrand om de tijd te wijzigen. Aanpassen hoeft niet op gsm.
- **Tijdspanne** — begin- en einduur instellen via `🕗 Tijden`.

## Opslaan & delen
- Alles wordt **automatisch lokaal opgeslagen** in de browser.
- **🔗 Delen** (aanbevolen) — de volledige planning wordt gecomprimeerd **in een link** gestopt. Geen bestand nodig:
  - **QR-code** — laat je collega scannen.
  - **WhatsApp-knop** — stuurt de link met één tik door.
  - **Kopieer** — plak de link waar je wil (mail, Teams…).
  - Op telefoon verschijnt ook **📤 Delen via toestel** (native deelmenu).
  - Wie de link opent, krijgt meteen alle zalen, kleuren, blokken en collega's te zien.
- **💾 Bestand** / **📂 Bestand openen** — als alternatief kan je nog steeds een `.json`-bestand exporteren/importeren.

> ⚠️ **Belangrijk voor de deel-link:** die werkt voor collega's pas wanneer de app **online** staat (een vast webadres). Open je `index.html` rechtstreeks vanaf je bureaublad (`file://`), dan werkt de link alleen op jouw eigen pc. Zie hieronder.

## Online zetten (zodat de deel-link werkt)
De app is een statische site (3 bestanden). Zet ze op een gratis host met een vast adres, bv. **GitHub Pages**. Daarna heeft iedereen met de link toegang — zonder bestanden door te sturen. Vraag gerust om dit op te zetten.

## Later: live cloud-sync (optioneel)
De deel-link is een momentopname. Wil je dat iedereen tegelijk in dezelfde planning bewerkt (live samen), dan is een servertje met gedeelde opslag nodig. Ook dat kan toegevoegd worden.
