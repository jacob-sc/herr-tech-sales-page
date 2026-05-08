# Sales-Page Template — Anweisung an Claude

> **Du bist hier, weil ein User dir den Repo-Link geteilt und gesagt hat: „Setz das lokal bei mir auf."**
> Diese Datei sagt dir, **wie du ihn Schritt für Schritt durchführst** — Beginner-Modus, keine Annahmen.

## 0. Vor allem anderen: Claude-Code-Check

**Bist du gerade in Claude Code Desktop?**
- Wenn der User in **Claude Chat** (claude.ai) oder **Cowork** ist → STOPP. Sag ihm:
  > *„Für lokales Setup brauchst du Claude Code Desktop — nur dort kann ich Dateien auf deinem Rechner anfassen. Lade das hier runter: https://claude.ai/download. Wenn du installiert hast, öffne Claude Code, klick auf den **Code**-Tab, wähl **Lokal** und such den Ordner `~/claude/` aus. Wirf den Repo-Link dann nochmal hier rein."*
- Wenn er Claude Code Desktop noch nicht installiert hat → führ ihn durch die Installation, bevor du irgendwas anderes machst.

**Hat der User ein globales `~/.claude/CLAUDE.md`?**
- Frag kurz: *„Hast du schon ein globales CLAUDE.md mit deinem Branding aufgesetzt?"*
- Wenn nein → biete an: *„Soll ich dir das vorher schnell anlegen? Das spart bei jedem Tool 5 Minuten Briefing."* (siehe Modul 3 Hebel 1 vom Starter Paket).
- Wenn ja → weiter mit Schritt 1.

## 1. Was wir hier tun — kurz erklären

Sag dem User in einem Satz:

> *„Wir setzen jetzt eine Sales-Page lokal bei dir auf. Eine HTML-Datei, kein Build, kein Hosting nötig — du kannst sie direkt im Browser anschauen und mit mir hier im Chat anpassen. Das geht in 3 Minuten."*

## 2. Repo klonen

Du machst das selbst:

```bash
cd ~/claude
git clone <REPO-URL> sales-page
cd sales-page
```

Erkläre dem User, was du gerade getan hast (1 Satz: *„Hab das Repo nach `~/claude/sales-page/` geklont, jetzt liegen alle Dateien lokal auf deinem Rechner."*).

## 3. Page im Browser öffnen

```bash
open index.html
```

Sag ihm: *„Browser sollte jetzt automatisch aufgehen — du siehst das Template-Beispiel (Claude-Startup-Sprint). Sag mir Bescheid wenn du es siehst."*

Warte auf Bestätigung. Wenn der Browser nicht aufgeht: Pfad checken, evtl. mit `open -a "Google Chrome" index.html` arbeiten.

## 4. Briefing für Anpassung holen

Frag den User:

> *„Geil. Jetzt passen wir's an dein Angebot an. Sag mir kurz:
> - **Was verkaufst du?** (1 Satz Produkt/Dienstleistung)
> - **Für wen?** (genaue Zielgruppe)
> - **Was kostet es?**
> - **3 Probleme**, die du löst
> - **3 Outcomes / Benefits**, die der Kunde bekommt
> - **Garantie / Risk-Reversal?** (z.B. 14 Tage Geld-zurück, optional)
> - **CTA-Ziel:** mailto, Cal.com-Link, Calendly?"*

## 5. Page anpassen

Wenn das Briefing da ist: Schreibe `index.html` um.
- Hero-Headline + Subline
- Pain-Block (3 Probleme)
- Benefits (3 Outcomes)
- Pricing-Sektion
- FAQ (5 häufige Einwände)
- CTA-Buttons (mailto / Cal.com / Calendly)
- Footer-Links (Impressum, Datenschutz — falls vorhanden, sonst Platzhalter)

**Wichtig:**
- Du-Ansprache, direkt, kurz, Herr-Tech-Stil (provokant, fragmentiert, FOMO)
- Mobile-first — alle Anpassungen müssen ab 375px gut aussehen
- Dark Theme + Lavendel-Akzent (`#A78BFA`) bleiben

Nach dem Schreiben: *„Lad die Page im Browser neu (Cmd+R / F5). Sag mir was passt und was nicht."*

## 6. Iteration

Lass den User iterieren. Üblich sind 3–5 Runden. Typische Anpassungen:
- *„Headline reißerischer"*
- *„Trust-Bar oben einfügen"*
- *„CTA häufiger platzieren"*
- *„Pricing klarer machen"*

Bei jedem Change: 1 Satz was du geändert hast, dann Browser-Reload-Hinweis.

## 7. Optional — Online stellen

Wenn der User Page online will, frag:

> *„Welche Domain hast du? Und gibt's einen Hoster, den du schon nutzt?"*

Standard-Empfehlung: **Netlify Drop** für Beginner. Schritt für Schritt:

1. Geh zu [app.netlify.com/drop](https://app.netlify.com/drop)
2. Zieh die `index.html` (oder den ganzen Ordner) ins Browser-Fenster
3. Netlify gibt dir sofort eine Live-URL (z.B. `random-name.netlify.app`)
4. Wenn du eigene Domain willst: in Netlify-Dashboard → **Domain Settings** → Domain hinzufügen → DNS-Anweisungen befolgen

Erkläre **jeden Klick**. Beginner-Modus.

## 8. Optional — DSGVO / Impressum / Datenschutz

Wenn der User in Deutschland live geht: Pflicht-Pages. Sag ihm:

> *„Für Deutschland brauchst du Impressum, Datenschutzerklärung und Cookie-Banner. Ich bau dir die Pflicht-Seiten — du musst nur deine Adresse, Steuer-ID und Kontakt-Email reingeben."*

Bau die zwei Seiten als `impressum.html` und `datenschutz.html`. Im Footer der `index.html` dorthin verlinken.

## Stilfragen für die Anpassung

- **Tonalität:** Herr-Tech-Stil → provokant, kurz, Du, fragmentiert. Beispiele: *„Vom Beginner zum Pro."* / *„Du nutzt Claude. Aber du nutzt es nicht."* / *„Kein YouTube-Tutorial. Kein Selbststudium."*
- **Floskeln vermeiden:** kein „wir freuen uns auf Sie", kein „herzlich willkommen", kein „selbstverständlich".
- **Emojis:** sparsam. Höchstens 1 pro Sektion, nicht mehr.

## Wenn der User feststeckt

- **Browser zeigt nichts:** Pfad prüfen mit `pwd`, dann `open index.html` mit absolutem Pfad
- **Tailwind-Klassen funktionieren nicht:** CDN-Script in `<head>` prüfen
- **Mobile sieht kaputt aus:** DevTools öffnen lassen (Cmd+Option+I → Mobile-Toggle)

Immer: *„Mach Screenshot von dem Problem, ich fix das."*
