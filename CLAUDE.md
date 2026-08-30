# CLAUDE.md – Glaubenssatz-Auflöser

Diese Datei gibt Claude Code Anweisungen für die Arbeit in diesem Repository.

---

## Was das hier ist

**Glaubenssatz-Auflöser** ist eine Landing Page für ein digitales Tool von **Cyclebreaker** (Marianne Hämmerle). Das Tool hilft Frauen, limitierende Glaubenssätze aufzulösen — mit einer strukturierten 5-Schritte-Anleitung basierend auf KI-Analyse.

**Produkt-Details:**
- **Format:** Single-Page Landing Page (HTML, CSS, JavaScript)
- **Preis:** 37€ einmalig
- **Integration:** PayPal-Zahlungen
- **Hosting:** Netlify
- **Zielgruppe:** Frauen, die ihre Glaubenssätze verstehen und transformieren möchten

---

## Workspace-Struktur

```
.
├── CLAUDE.md              # Diese Datei — Projektkontext und Anweisungen
├── index.html             # Komplette Landing Page (HTML + CSS + JS)
├── netlify.toml           # Netlify Deployment-Konfiguration
├── .claude/
│   ├── commands/          # Benutzerdefinierte Commands
│   └── skills/            # Wiederverwendbare Skills
├── context/               # Projektkontext & Strategie
├── content/               # Texte, Kopien, Messaging
├── design/                # Design-Referenzen & Farb-Palette
├── outputs/               # Deliverables, Reports, Analysen
├── plans/                 # Implementierungspläne
├── reference/             # Vorlagen & Patterns
└── scripts/               # Automatisierungen (falls zutreffend)
```

---

## Wichtige Dateien & Ihre Funktion

| Datei           | Zweck                                                           |
|-----------------|--------------------------------------------------------------:|
| `index.html`    | Komplette Landing Page — HTML, CSS, PayPal-JS, alle Copy      |
| `netlify.toml`  | Deploy-Konfiguration, Redirects, Umgebungsvariablen          |
| `context/`      | Strategie, Ziele, Zielgruppe-Infos                            |
| `content/`      | Texte, Headlines, Messaging — Quelle der Wahrheit           |
| `design/`       | Farb-Palette, Typography, Design System                      |
| `outputs/`      | Reports, Analytics, Performance-Data, Optimierungsergebnisse |
| `reference/`    | Best Practices, A/B-Test-Templates, Conversion-Patterns      |

---

## Design-System & Farben

Das Projekt nutzt eine **klassisch-warme Farbpalette**:

```css
--bg: #f7f2e7               /* Beige-Hintergrund */
--bg-soft: #efe6d3          /* Helleres Beige */
--accent: #E87722           /* Orange (Hauptakzent) */
--accent-light: #c9600f     /* Dunkeleres Orange */
--gold: #b8862a             /* Gold (Akzente) */
--ink: #1a1410              /* Dunkelbraun (Text) */
--card: #fffdf8             /* Kartenfarbe */
```

**Typografie:**
- Überschriften: Cinzel (elegant, serifen)
- Body-Text: Cormorant Garamond (warm, serifen)

---

## Arbeitsabläufe

### Landing Page optimieren

Bei Änderungen an `index.html`:

1. **Prüfe die Struktur**: Sections, HTML-Semantik, Responsivität
2. **CSS anpassen**: Nur inline `<style>` — keine externen Dateien
3. **Testing**: Browser (Desktop + Mobile), verschiedene Schriftgrößen
4. **PayPal-Integration**: Nicht anfassen ohne explizite Anweisung
5. **SEO prüfen**: Meta-Tags, Structure, Descriptions

### Texte/Copy aktualisieren

Alle Copy (Headlines, Descriptions, CTAs) sind im HTML. Für Änderungen:

1. Lese die aktuelle Version in `index.html`
2. Bearbeite die Copy im entsprechenden `<section>`
3. Prüfe Ton, Länge, Whitespace
4. Commit mit klarer Botschaft

### Neue Features hinzufügen

Vor Änderungen an der Seite:

1. Verwende `/create-plan [Feature]` zum Planen
2. Überprüfe auf Auswirkungen auf Konvertierungsrate
3. Dokumentiere Änderungen in `outputs/`
4. Teste gründlich vor dem Push

---

## PayPal-Integration

**Wichtig:** Die PayPal-Integration ist über einen Hosted Button verankert:
- Button ID: `PWCRJYLB8T7SA`
- Client ID: Im `<script src>` gehostet
- Checkbox für Widerrufrecht erforderlich vor Zahlung

⚠️ **Nur ändern mit Zustimmung des Produktbesitzers.**

---

## Deployment (Netlify)

Die Seite deployed automatisch bei Push zu `main`:

- **Build Command:** `echo 'Static site - no build needed'`
- **Publish Directory:** `.` (Root)
- **Redirects:** SPA-Mode aktiviert (`/*` → `/index.html`)

---

## Kontakt & Ressourcen

- **Produktbesitzer:** Marianne Hämmerle
- **Website:** https://marianne-haemmerle.at
- **AGB/Impressum:** Verlinkt im Footer der Landing Page
- **Datenschutz:** https://marianne-haemmerle.at/datenschutz

---

## Für zukünftige Sessions

Starte jede Session mit dem Kontext dieser Datei. Frage:
- Wie lautet die aktuelle Aufgabe?
- Welche Datei/Section ist betroffen?
- Beeinträchtigt die Änderung Konvertierung oder User Experience?

**Diese Datei aktualisieren** wenn:
- Neue Ordner/Struktur hinzugefügt werden
- Workflows sich ändern
- Neue Tools oder Prozesse eingeführt werden
