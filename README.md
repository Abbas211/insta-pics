# insta-pics

Öffentlicher Bild-Host für die Instagram-Veröffentlichung von **KassenIQ** (`@kasseniq.de`).

Die Instagram Graph API lädt Bilder beim Veröffentlichen **selbst herunter** und braucht dafür
eine öffentlich erreichbare URL im Format **JPEG** (max. 8 MB, Seitenverhältnis zwischen 4:5
und 1.91:1). Genau dafür existiert dieses Repository — mehr nicht.

## Inhalt

| Ordner | Inhalt |
|---|---|
| `posts/` | Feed-Grafiken 1080×1080, JPEG (Qualität 92) |
| `reels/` | Reels 1080×1920, MP4 (H.264) + Cover als JPEG |

## URL-Schema

Bilder über `raw.githubusercontent.com`:

```
https://raw.githubusercontent.com/Abbas211/insta-pics/main/posts/<name>.jpg
```

Videos **nicht** über `raw.githubusercontent.com` — der liefert MP4 als
`application/octet-stream` aus, womit die Veröffentlichung scheitert. Stattdessen den
jsDelivr-Spiegel desselben Repositories, der `video/mp4` setzt:

```
https://cdn.jsdelivr.net/gh/Abbas211/insta-pics@main/reels/<name>.mp4
```

> **Ersetzte Dateien nicht überschreiben, sondern neu benennen.** jsDelivr cacht pro Pfad;
> gleicher Pfad mit neuem Inhalt kann noch die alte Fassung ausliefern.

## Herkunft

Die Bilder werden **nicht hier** bearbeitet. Quelle und Renderpipeline liegen im
Hauptprojekt unter `docs/04-business/marketing/instagram/` (`build.js` erzeugt HTML,
Chromium rendert PNG). Dieses Repository enthält nur die JPEG-Ableitungen zum Ausliefern.
Änderungen also immer dort vornehmen und die JPEGs neu ableiten.

## Regeln für dieses Repository

- **Nur veröffentlichungsreife Bilder.** Alles hier ist öffentlich lesbar.
- Keine Captions, keine Strategie, keine Kalkulationen, keine Kundendaten, keine Zugangsdaten.
- Keine Entwürfe, die nicht gepostet werden sollen — was hier liegt, kann jeder sehen.
