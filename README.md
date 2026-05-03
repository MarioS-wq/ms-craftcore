# Mario Stefek – Webseite

Diese Webseite ist **technisch ready to launch**. Sie können sie direkt auf jeden gängigen Webspace hochladen und sie funktioniert.

Bevor Sie sie online stellen, müssen Sie aber noch **ein paar Stellen ausfüllen** (Impressum, AGB) und **echte Inhalte** ergänzen (Testimonials). Dafür ist diese Checkliste da.

---

## 📁 Was ist in diesem ZIP

```
mario-stefek-website/
├── index.html          ← Hauptseite
├── impressum.html      ← Impressum (mit Platzhaltern)
├── datenschutz.html    ← Datenschutzerklärung
├── agb.html            ← AGB
├── 404.html            ← Fehlerseite
├── style.css           ← Komplettes Stylesheet (alle Seiten teilen sich das)
├── robots.txt          ← Anweisung für Suchmaschinen
├── sitemap.xml         ← Inhaltsverzeichnis für Google
├── README.md           ← Diese Datei
└── img/
    ├── mario-handshake-baustelle.jpg
    ├── mario-portrait-baustelle.jpg
    ├── mario-bauplan.jpg
    └── mario-heizung.jpg
```

---

## ✅ Launch-Checkliste – DAS müssen Sie noch machen

### 1. Persönliche Daten ausfüllen (PFLICHT)

Suchen Sie in den Dateien nach den **eckigen Klammern `[…]`** und ersetzen Sie sie durch echte Daten.

**In `impressum.html`:**
- `[Straße und Hausnummer]`
- `[PLZ und Ort]`
- `[ihre-email@domain.at]` (an 1 Stelle)
- `[ATU-Nummer einfügen]`
- `[Bundesland]` (für Wirtschaftskammer)
- `[Ort]` (für Aufsichtsbehörde)

**In `datenschutz.html`:**
- `[Straße und Hausnummer]`
- `[PLZ und Ort]`
- `[ihre-email@domain.at]` (an 1 Stelle)

> ⚠️ **Wichtig:** Ohne korrektes Impressum drohen Abmahnungen. Daten **vor** dem Launch ausfüllen.

### 2. Domain festlegen und Meta-Daten anpassen

Wenn Sie Ihre finale Domain wissen (z. B. `mario-stefek.at` oder `mario-stefek.com`), müssen folgende Stellen angepasst werden:

**In allen `.html`-Dateien:** Den Platzhalter `https://www.mario-stefek.com` durch Ihre echte Domain ersetzen. Betroffene Stellen:
- `<link rel="canonical" href="…">`
- `<meta property="og:url" content="…">`
- `<meta property="og:image" content="…">`
- `<meta name="twitter:image" content="…">`
- Im JSON-LD-Block: `"url"` und `"image"`

**In `sitemap.xml`:** Alle vier `<loc>`-URLs auf Ihre Domain anpassen.

**In `robots.txt`:** Die Sitemap-Zeile auf Ihre Domain anpassen.

> 💡 **Schnell-Trick:** In jedem Code-Editor (z. B. VS Code, Notepad++) gibt es eine "In allen Dateien suchen & ersetzen"-Funktion. Suchen: `www.mario-stefek.com` → Ersetzen: `ihre-echte-domain.at`

### 3. Echte Testimonials einsetzen (DRINGEND empfohlen)

In `index.html` → Sektion `<!-- ⚠️ HIER ECHTE TESTIMONIALS EINSETZEN -->` finden Sie 3 Platzhalter mit:
- `[Echter Kundenname]`
- `[Gewerk] · [Mitarbeiter] · [Region] · [Dauer als Partner]`

**Sammeln Sie 3 echte Kundenstimmen** (mit schriftlichem Einverständnis!) und tragen Sie diese ein. Aktuell stehen nur die *Zitate* drin (die könnten so geblieben sein, falls sie zu echten Kunden passen).

> ⚖️ **Rechtlicher Hinweis:** Erfundene Testimonials sind in DE/AT wettbewerbsrechtlich riskant (UWG). Bitte ersetzen Sie sie vor dem Launch durch echte.

### 4. Telefonnummer prüfen

Die Nummer **+43 660 8640360** ist überall hinterlegt. Falls Sie eine andere Nummer nutzen möchten:

In allen Dateien (`.html`) **drei Schreibweisen** ändern:
- `tel:+436608640360` (Klick-zu-Anruf-Links)
- `+43 660 8640360` (sichtbarer Text)
- `wa.me/436608640360` (WhatsApp-Links — **ohne** Plus, **ohne** Leerzeichen!)

### 5. WhatsApp-Funktion testen

Die WhatsApp-Integration funktioniert sofort. Testen Sie:
1. Öffnen Sie `index.html` im Browser
2. Klicken Sie auf den **grünen WhatsApp-Button unten rechts** → öffnet WhatsApp Web/App mit vorgefertigter Nachricht
3. Im Formular alle Felder ausfüllen → "Per WhatsApp senden" → öffnet WhatsApp mit allen Daten als Text

Sie bekommen die Nachricht direkt auf Ihrem WhatsApp-Konto. Kein Backend, keine Server-Konfiguration nötig.

### 6. Datenschutzerklärung von einem Anwalt prüfen lassen (empfohlen)

Die Datenschutzerklärung deckt Standardfälle ab und enthält bereits den **WhatsApp-Datenschutz-Hinweis** (Drittland-Übermittlung, Meta etc.). Trotzdem empfehle ich, sie einmal von einem Datenschutzanwalt oder einem Tool wie eRecht24 / WKO-Vorlage prüfen zu lassen, **besonders weil WhatsApp Daten in die USA überträgt**.

---

## 🚀 So bringen Sie die Seite online

### Variante A: Eigener Webspace (z. B. World4You, Hetzner, IONOS, Strato)

1. Per FTP/SFTP auf Ihren Webspace verbinden (Programme: FileZilla, Cyberduck)
2. **Alle Dateien** aus diesem ZIP ins Hauptverzeichnis (`htdocs/`, `public_html/` oder `www/`) hochladen
3. Wichtig: Den `img/`-Ordner mit hochladen!
4. Domain darauf zeigen lassen
5. Fertig – die Seite ist erreichbar.

### Variante B: Netlify, Vercel, Cloudflare Pages (kostenlos, einfach)

1. Account anlegen
2. ZIP per Drag & Drop ins Browser-Fenster ziehen
3. Domain verbinden
4. Fertig

---

## 📞 Was Sie dann auf Anfragen tun müssen

Wenn jemand Ihnen über die Seite eine WhatsApp-Nachricht schickt, sieht das so aus:

```
Hallo Mario,

ich hätte gerne ein Erstgespräch zu Ihrer Auftragsvermittlung.

• Name & Betrieb: Thomas Huber, Huber Haustechnik
• Telefon: +43 664 1234567
• Gewerk: Sanitär, Heizung, Klima
• PLZ: 1010

Bitte um Rückmeldung. Danke!
```

Sie haben dann alle Daten, um zurückzurufen.

---

## 🎨 Design-Hinweise

Die Seite wurde **gezielt für Handwerksbetriebs-Inhaber** gestaltet:
- **Werkstatt-Ästhetik** statt Agentur-Look (Papierbeige, Tinten-Schwarz, gebranntes Orange)
- **Klartext-Sprache** statt Marketing-Phrasen
- **Klick-zu-Anruf** als wichtigster CTA (Inhaber rufen lieber an als zu tippen)
- **Mario im Handwerker-Kontext** auf den Bildern – er muss als "einer von uns" wahrgenommen werden, nicht als Marketing-Mensch
- **WhatsApp-First** als Sekundär-Kontakt (auf der Baustelle leichter als E-Mail)

Wenn Sie an Texten oder Bildern noch etwas ändern wollen: Beide hängen in `index.html`. Suchen Sie einfach nach dem Text, der geändert werden soll, im Editor.

---

## ❓ Bei Fragen

Falls etwas an der Seite nicht funktioniert oder Sie etwas ändern wollen, kommen Sie auf den Bot zurück, der diese Seite gebaut hat – die Code-Struktur ist sauber und einfach erweiterbar.

**Stand:** Mai 2026
