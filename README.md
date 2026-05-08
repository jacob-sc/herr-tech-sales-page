# 💰 Sales-Page Template

Eine konvertierende Landing-Page als **eine HTML-Datei**. Du füllst den Inhalt mit Claude — keine Programmierung, kein Build, kein Deploy-Stress.

## Was das ist

- **`index.html`** — die komplette Sales-Page in einer einzigen Datei
- Mobile-friendly, Dark Theme, Lavendel als Akzent
- Fertige Sektionen: Hero · Marquee · Pain Points · Benefits · How it works · Social Proof · Pricing · FAQ · CTA · Footer
- Animationen (Scroll-Reveal, Sticky-CTA, Glow-Buttons) sind schon drin
- Tailwind CSS lädt direkt über CDN — kein `npm install` nötig

Das Template ist mit dem **Claude Startup Sprint** als Beispiel gefüllt. Du brauchst nur Claude zu sagen: *„pass das an mein Angebot an"* — er ändert Headline, Pain Points, Pricing, FAQ, Testimonials.

## Was du brauchst

- **Claude Code Desktop** — [claude.ai/download](https://claude.ai/download)
- Ein Browser (zum Anschauen)

Mehr nicht. Kein Node.js, keine APIs, keine Accounts.

## Setup in 3 Schritten

### 1. Repo klonen

In **Claude Code Desktop** sagst du:

> *„Setz das Sales-Page-Template lokal bei mir auf: https://github.com/jacob-sc/herr-tech-sales-page"*

Claude klont das Repo nach `~/claude/sales-page/` und öffnet `index.html` für dich.

> ℹ️ Falls du gerade in **Claude Chat** oder **Cowork** bist: erst Claude Code Desktop öffnen. Nur dort kann der Code lokal auf deinem Rechner laufen.

### 2. Im Browser öffnen

```bash
open index.html
```

Oder: Doppelklick auf `index.html` im Finder. Die Page öffnet im Browser. Du siehst das Template-Beispiel (Claude-Coaching).

### 3. Inhalt anpassen

Sag Claude im selben Chat:

> *„Pass die Page an mein Angebot an:
> - Was ich verkaufe: \[Produkt/Dienstleistung]
> - Für wen: \[Zielgruppe]
> - Pricing: \[Preis]
> - 3 Pain Points die ich löse: …
> - 3 Benefits / Outcomes: …"*

Claude schreibt Headline, Pain Points, Benefits, FAQ direkt in `index.html` um. Browser neu laden — fertig.

## Iterieren — der Hebel

Erste Version ist nie perfekt. Sag Claude einfach:

- *„Headline reißerischer"*
- *„Trust-Bar oben mit ★ 4.9 und Kunden-Anzahl"*
- *„Pricing-Sektion mit Ratenzahlung-Option"*
- *„FAQ um 3 Fragen erweitern: …"*

Iterier 3–5×. Die 5. Version ist 500 % besser als die 1.

## Online stellen

Wenn die Page steht, sag Claude:

> *„Ich will die Page mit meiner eigenen Domain online stellen. Welcher Hosting-Anbieter eignet sich? Führ mich Schritt für Schritt durch Hosting-Setup, Domain-Verknüpfung und Upload."*

Claude empfiehlt **Netlify**, **Vercel** oder **Cloudflare Pages** (alle kostenlos für Landing-Pages) und führt dich Schritt für Schritt durch:
- Account anlegen
- Datei hochladen
- Eigene Domain dranhängen

## DSGVO / Impressum / Datenschutz

Pflicht in Deutschland. Sag Claude:

> *„Was muss ich für Deutschland rechtlich beachten? Cookie-Banner, Impressum, Datenschutz. Bau das ein und führ mich durch was ich selbst eintragen muss."*

## Platzhalter, die du noch tauschen musst

Diese Sachen sind im Template als Beispiel drin und müssen vor Launch raus:

- [ ] **mailto-Links** (`hello@example.com`) → deine echte E-Mail oder ein Booking-Link (Cal.com, Calendly)
- [ ] **Testimonials** (Max Klein, Sarah Rauch, Jana Hofer) → echte Kundenstimmen
- [ ] **Footer-Links** (Impressum, Datenschutz, Kontakt) → echte Seiten verlinken
- [ ] Optional: **Avatar-Initialen** durch echte Fotos ersetzen

Sag einfach: *„Ersetze die Platzhalter mit \[deinen Daten]"* — Claude weiß was zu tun ist.

## Troubleshooting

**Page sieht im Browser kaputt aus?**
Manche Browser blocken die Tailwind-CDN bei lokalen Dateien. Prüf in Claude Code:
> *„Die Page lädt nicht richtig — was ist los?"*
Claude öffnet die Browser-Console und debugged.

**Die Animationen ruckeln?**
Auf älteren Rechnern können Blob-Animationen schwer laufen. Sag Claude:
> *„Animationen reduzieren, Performance-optimiert"*

**Mobile sieht komisch aus?**
> *„Mach mal Screenshot vom Mobile-View und fix die Probleme"*
Claude nutzt die Browser-DevTools für Mobile-Preview und fixt die Layout-Issues.

---

> Teil von [Herr Tech Starter Tools](../README.md) — Modul 3 vom Claude Code Starter Paket.
