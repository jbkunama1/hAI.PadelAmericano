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

## 🧠 Turnierformate & Logik

Padel-Turniere im Freizeitbereich folgen meist einem von mehreren verwandten Formaten. Allen gemeinsam: gespielt wird **im Doppel (2 vs. 2)**, gewertet wird aber **individuell**. Die App unterstützt das Americano-Format und erklärt die Logik der verwandten Formate, damit du das Passende für deine Gruppe wählen kannst.

---

### 🎲 Americano (Klassisch)

Das **Grundformat** – einfach, sozial, für alle Niveaus geeignet.

**Ablauf:**
1. Alle Paarungen werden **zufällig** ausgelost – in jeder Runde neue Partner und neue Gegner.
2. Jedes Match wird bis zu einer **festen Punktzahl** gespielt (typisch: 16, 24 oder 32 Punkte).
3. Nach jedem Match werden die Punkte **direkt den einzelnen Spielern** gutgeschrieben.
4. Das Turnier endet nach einer festgelegten Anzahl Runden oder wenn jeder gegen jeden gespielt hat.

**Beispiel-Wertung:**  
Match endet 14:10 → Spieler A & B bekommen je **14 Punkte**, Spieler C & D je **10 Punkte**.

**Aufschlagregel:**  
Das aufschlagende Team wechselt alle 2–4 Punkte (je nach Hausregel). Jeder Ball zählt als 1 Punkt.

**Ideal für:** lockere Gruppen, Schulklassen, Vereinsabende, Spieler aller Stärken.

---

### ⚡ Mexicano

Eine **dynamische Weiterentwicklung** des Americano – mit automatischer Anpassung nach Leistung.

**Der entscheidende Unterschied zum Americano:**  
Ab der zweiten Runde werden Paarungen **nicht mehr zufällig** bestimmt, sondern basierend auf der **aktuellen Rangliste**:

- Rang 1 & 3 spielen **zusammen** gegen Rang 2 & 4
- Rang 5 & 7 spielen **zusammen** gegen Rang 6 & 8
- usw.

So entstehen zunehmend **ausgeglichene Matches** – starke Spieler treffen auf starke, schwächere auf ähnlich Starke.

**Ablauf:**
1. **Runde 1:** zufällige Auslosung (wie Americano)
2. **Ab Runde 2:** Paarung nach aktuellem Ranking (1+3 vs. 2+4, 5+7 vs. 6+8 …)
3. Wertung identisch zum Americano – individuelle Punkte pro Match

> ⚠️ Im Mexicano kann man **mit oder gegen denselben Spieler mehrmals** spielen – das ist systembedingt und kein Fehler.

**Ideal für:** Gruppen mit **gemischten Leistungslevels**, die trotzdem faire Matches wollen.

---

### 👫 Mixed Americano

Wie klassisches Americano, aber mit **erzwungener Geschlechterdurchmischung**.

**Regeln:**
- Jedes Team besteht immer aus **genau einem Mann und einer Frau** (Mixed Doubles).
- Gleiche Anzahl männlicher und weiblicher Spieler erforderlich (mind. je 4, also 8 gesamt).
- Wechselnde Partner nach jeder Runde – aber immer Mixed.
- Am Ende wird **getrennt gewertet**: bester Herr und beste Dame gewinnen jeweils.

**Ideal für:** Vereinsabende, gemischte Gruppen, inklusive Formate.

---

### 🌮 Mixed Mexicano

Kombination aus **Mexicano-Dynamik** und **Mixed-Doubles-Pflicht**.

- Paarungen ab Runde 2 nach aktuellem Ranking – aber jedes Team muss **1 Mann + 1 Frau** sein.
- Die Rangliste läuft getrennt oder gemischt (je nach Hausregel).
- Besonders geeignet, wenn das Leistungsniveau zwischen Männern und Frauen vergleichbar ist.

**Ideal für:** fortgeschrittene gemischte Gruppen, die sowohl Fairness als auch Dynamik wollen.

---

### 🤝 Team Americano / Team Mexicano

Varianten, bei denen **feste Teams** (vorher bestimmt) durch das gesamte Turnier spielen.

| Merkmal | Individual (Standard) | Team-Variante |
|---|---|---|
| Partner | wechselt jede Runde | fest für das ganze Turnier |
| Wertung | pro Spieler | pro Team |
| Strategie | soziales Mischen | Teambuilding, Vereinspokal |
| Paarung | zufällig (Americano) / Ranking (Mexicano) | gleiche Mechanik |

**Ideal für:** Vereinspokale, Firmenturniere, wenn Teams als Einheit antreten sollen.

---

### 📊 Formatvergleich auf einen Blick

| Format | Paarung | Partner | Niveau-Ausgleich | Wertung |
|---|---|---|---|---|
| Americano | zufällig | wechselnd | ❌ | individuell |
| Mexicano | Ranking-basiert | wechselnd | ✅ | individuell |
| Mixed Americano | zufällig, Mixed | wechselnd | ❌ | individuell (getrennt) |
| Mixed Mexicano | Ranking-basiert, Mixed | wechselnd | ✅ | individuell |
| Team Americano | zufällig | fest | ❌ | pro Team |
| Team Mexicano | Ranking-basiert | fest | ✅ | pro Team |

---

### 🏟️ Spieleranzahl & Courts

| Spieler | Courts | Pause pro Runde | Empfohlenes Format |
|---------|--------|-----------------|-------------------|
| 4 | 1 | keine | Americano |
| 6 | 1 | 2 Spieler | Americano |
| 8 | 2 | keine | Americano / Mexicano |
| 10 | 2 | 2 Spieler | Mexicano |
| 12 | 3 | keine | Mexicano |
| 16+ | 4+ | keine | Mexicano / Mixed |

Ist die Spielerzahl **nicht durch 4 teilbar**, pausiert pro Runde eine Gruppe. Die App verteilt Pausen möglichst gleichmäßig auf alle Spieler.

---

### 🏆 Wertung & Rangliste (alle Formate)

- Jedes Match wird bis zu einer festen Punktzahl gespielt – üblich sind **16, 24 oder 32 Punkte**.
- Alternativ kann ein **Zeitlimit** (10–20 Minuten) gesetzt werden.
- Der Aufschlag wechselt alle **2–4 Punkte** zum Gegner.
- Jeder gewonnene Ball = **1 Punkt** für das entsprechende Team.
- Diese Punkte werden nach Matchende **direkt auf die beteiligten Einzelspieler** übertragen.
- Die **Rangliste** sortiert nach: Gesamtpunkte → Spielanzahl → Punktedifferenz.

---

## ✨ Funktionen der App

- 🎲 **Americano-Auslosung** – automatische Runden mit Doppel-Teams.
- 📋 **Match-Verwaltung** – Punkte pro Match und Platz eintragen.
- 🧮 **Live-Rangliste** – Einzelwertung nach Punkten, Spielen und Differenz.
- 🖥️ **Monitor-Modus** – Vollbild-nahe Anzeige für TV/Beamer.
- 💾 **JSON Import/Export** – Turniere lokal sichern und später wieder laden.
- 🌐 **100 % statisch** – läuft komplett im Browser, kein Server nötig.

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

Da die App **100 % statisch** ist (reines HTML/CSS/JS), gibt es mehrere einfache Wege, sie bereitzustellen:

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
