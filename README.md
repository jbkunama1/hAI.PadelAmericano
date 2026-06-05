# hAI Padel Americano 🎾🧠

> Ein schlanker Turnier-Manager für **Padel Americano** – ideal für Vereine, Schulen und Freundeskreise.

<div align="center">
  <img src="hai-padel-banner.png" alt="hAI Padel Americano Banner" width="480" />
</div>

<p align="center">
  <img src="https://img.shields.io/badge/padel-americano-22c55e?style=for-the-badge&logo=google-forms&logoColor=ffffff" alt="Padel Americano" />
  <img src="https://img.shields.io/badge/status-prototyp-blue?style=for-the-badge" alt="Status Prototype" />
  <img src="https://img.shields.io/badge/license-MIT-green?style=for-the-badge" alt="MIT License" />
</p>

<p align="center">
  <img src="https://img.shields.io/github/languages/top/jbkunama1/hAI.PadelAmericano?color=38bdf8&label=main%20stack&style=flat-square" alt="Main Stack" />
  <img src="https://img.shields.io/github/last-commit/jbkunama1/hAI.PadelAmericano?style=flat-square&color=f97316" alt="Last Commit" />
  <a href="https://github.com/jbkunama1/hAI.PadelAmericano/actions/workflows/trufflehog.yml"><img src="https://img.shields.io/github/actions/workflow/status/jbkunama1/hAI.PadelAmericano/trufflehog.yml?label=TruffleHog%20Scan&logo=github&logoColor=white&style=flat-square" alt="TruffleHog Scan" /></a>
  <img src="https://img.shields.io/badge/security-secrets%20scan%20enabled-brightgreen?logo=trustpilot&logoColor=white&style=flat-square" alt="Security" />
</p>

---

## 🧠 Americano-Logik

Padel Americano ist ein geselliges Turnierformat, bei dem **alle gegen alle** spielen – aber immer in wechselnden Doppel-Konstellationen. Das Besondere: Gewertet wird **individuell**, nicht als Team.

### Grundprinzip

- Gespielt wird in Doppeln (2 vs. 2).
- Nach jedem Match werden die Partner und Gegner neu ausgelost.
- Ziel ist eine möglichst faire Durchmischung – jede Person soll mit und gegen möglichst viele andere spielen.
- Die erzielten Punkte (z. B. 32:28 = 32 Punkte für Team A, 28 für Team B) werden **direkt den einzelnen Spielern** gutgeschrieben.

### Spieleranzahl & Pausen

| Spieler | Courts | Pause pro Runde |
|---------|--------|-----------------|
| 4 | 1 | keine |
| 8 | 2 | keine |
| 6 | 1 | 2 Spieler |
| 10 | 2 | 2 Spieler |
| 12 | 3 | keine |

Ist die Spielerzahl **nicht durch 4 teilbar**, pausiert pro Runde automatisch eine Gruppe (meist 2 Personen). Die App verteilt Pausen so gleichmäßig wie möglich.

### Auslosungsmöglichkeiten

Die App unterstützt zwei Modi:

- **Zufällige Auslosung** – Partner und Gegner werden pro Runde per Zufall neu gemischt. Ideal für lockere Runden mit Freunden oder Schulklassen.
- **Heuristische Optimierung** – Die App versucht, Wiederholungen (gleiche Partner / gleiche Gegner) zu minimieren. Empfohlen ab 6+ Spielern für ein faireres Erlebnis.

> ⚠️ Die Auslosung garantiert kein perfektes mathematisches Rundenschema, da dies bei vielen Spielerzahlen kombinatorisch nicht exakt lösbar ist.

### Wertung & Rangliste

- Punkte werden nach jedem Match für alle vier beteiligten Spieler eingetragen.
- Die **Rangliste** sortiert nach: Gesamtpunkten → Anzahl Spiele → Punktedifferenz.
- Optional: Siege können zusätzlich als Bonus gezählt werden (konfigurierbar).

---

## ✨ Funktionen

- 🎲 **Americano-Auslosung** – automatische Runden mit Doppel-Teams.
- 📋 **Match-Verwaltung** – Punkte pro Match und Platz eintragen.
- 🧮 **Live-Rangliste** – Einzelwertung nach Punkten, Spielen und Differenz.
- 🖥️ **Monitor-Modus** – Vollbild-nahe Anzeige für TV/Beamer.
- 💾 **JSON Import/Export** – Turniere lokal sichern und später wieder laden.
- 🌐 **100 % statisch** – läuft komplett im Browser, kein Server nötig.

---

## 📦 Projektstruktur

```text
hAI.PadelAmericano/
├── index.html      # Web-App (UI + Logik)
├── README.md       # README (Deutsch)
├── README_en.md    # README (Englisch)
├── LICENSE
└── .gitignore
```

---

## 🚀 Deployment

Da die App **100 % statisch** ist (reines HTML/CSS/JS), gibt es mehrere einfache Wege, sie bereitzustellen:

### ⭐ GitHub Pages (empfohlen)

Die einfachste und kostenlose Option – direkt aus dem Repository heraus:

1. Repository auf GitHub öffnen → **Settings** → **Pages**
2. Source: **Deploy from a branch** → Branch `main`, Ordner `/ (root)`
3. Speichern – nach wenigen Minuten ist die App erreichbar unter:

```
https://jbkunama1.github.io/hAI.PadelAmericano/
```

> 💡 Bei Änderungen am `main`-Branch wird die Seite automatisch neu deployed.

### Lokal per HTTP-Server

```bash
git clone https://github.com/jbkunama1/hAI.PadelAmericano.git
cd hAI.PadelAmericano
python3 -m http.server 8000
# → http://localhost:8000/index.html
```

### Eigener Webserver / Self-Hosted

Die `index.html` kann direkt in jeden Webserver-Ordner (Apache, Nginx, Caddy) gelegt werden – keine Build-Tools oder Abhängigkeiten nötig.

### Docker / Portainer

Für eine containerisierte Variante genügt ein einfaches Nginx-Image:

```yaml
# docker-compose.yml
services:
  padel:
    image: nginx:alpine
    ports:
      - "8080:80"
    volumes:
      - ./:/usr/share/nginx/html:ro
```

```bash
docker compose up -d
# → http://localhost:8080/index.html
```

---

## 📜 Lizenz (MIT)

Dieses Projekt steht unter der **MIT-Lizenz** – Nutzung, Veränderung und Weitergabe sind frei erlaubt, solange Urheberrechtshinweis und Lizenztext erhalten bleiben.

Der vollständige Lizenztext befindet sich in der Datei `LICENSE`.
