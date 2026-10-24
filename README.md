# Animationen Wechselstromtechnik

Interaktive HTML-Animationen für den Unterricht in der Elektrotechnik. Jede Animation ist eine eigenständige HTML-Datei ohne externe Abhängigkeiten. Die Seite ist rein statisch und braucht keinen Server mit Programmiersprache oder Datenbank.

## Inhalt

| Ordner | Thema |
| --- | --- |
| `induktionsgesetz/` | Magnet dreht sich über einer Spule, Fluss und induzierte Spannung am Oszilloskop |
| `zeigerdiagramm/` | Drehstromgenerator mit Zeigerdiagramm, Liniendiagramm und Momentanwerten |

## Struktur

```
index.html            Landingpage mit Links zu allen Animationen
impressum.html        Vorlage, vor Veröffentlichung ausfüllen
datenschutz.html      Vorlage, vor Veröffentlichung ausfüllen
assets/style.css      Gemeinsames Layout für Landingpage und Rechtstexte
<thema>/index.html    eine Animation pro Ordner
```

## Neue Animation hinzufügen

1. Ordner anlegen, z. B. `blindleistung/`, und die Animation als `index.html` hineinlegen.
2. Keine externen Schriften oder CDNs einbinden (Datenschutz). Systemschrift verwenden.
3. Oben einen Rücklink einfügen: `<a href="../">← Zur Übersicht</a>`.
4. In `index.html` eine weitere Kachel (`<a class="card">`) ergänzen.

## Vor der Veröffentlichung

- Gelb markierte Platzhalter in `impressum.html` und `datenschutz.html` ausfüllen.
- In `datenschutz.html` die passende Hosting-Variante behalten, die andere löschen.
- Keine Screenshots, Grafiken oder Texte aus Schulbüchern ins Repository legen.

## Veröffentlichen

**GitHub Pages:** Repository auf GitHub anlegen und pushen. Unter *Settings → Pages* als Quelle den Branch `main` und den Ordner `/ (root)` wählen. Die Seite ist danach unter `https://<benutzer>.github.io/<repository>/` erreichbar.

**Eigener Server mit Caddy:**

```
animationen.example.de {
    root * /srv/animationen-wechselstrom
    file_server
}
```

Aktualisieren mit `git pull` im Zielordner.

## Lizenz

Inhalte (Texte, Grafiken, Animationen als Lernmaterial): CC BY 4.0
Code (HTML, CSS, JavaScript): MIT

Details in `LICENSE`.
