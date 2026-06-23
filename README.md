# Canzler Digital — Website

Statische Website (reines HTML/CSS, kein Build-Prozess, kein Framework) für "Canzler Digital" — Prozessberatung für kleine Handwerksbetriebe und Hausverwaltungen im Raum Esslingen.

## Status
Funktionsfähige erste Version. Inhalt und Struktur sind final abgestimmt, Design ist bewusst zurückhaltend gehalten. Bereit zum Deployment auf Cloudflare Pages.

## Dateien
```
index.html   → Gesamte Seite: Header, Hero, Problem-Szenen, Angebot, So funktioniert's, Preis, Kontakt, Footer
style.css    → Alle Styles, mobile-first reflow ab 640px
```
Keine weiteren Abhängigkeiten. Keine Build-Tools, kein npm nötig — die Dateien können 1:1 auf jeden statischen Hoster hochgeladen werden.

## Design-System (bitte bei Änderungen beibehalten)

**Signatur-Element:** das "Siegel-Lockup" — Name und Claim als feste, gerahmte Einheit (`.lockup` Klasse). Name und Claim dürfen NIE als zwei unabhängige, getrennte Zeilen erscheinen (das wurde im Designprozess bewusst verworfen). Der Rahmen hält beides zusammen, auf jeder Bildschirmgröße.

**Farben:**
- `--paper: #faf8f4` (Hintergrund)
- `--ink: #1c2526` (Haupttext, fast Schwarz mit Blaugrün-Stich)
- `--petrol: #3d5a52` (Akzent — NICHT Terrakotta/Orange, das war eine bewusste Abkehr vom "KI-Standardlook")
- `--leather: #8b7355` (Sekundärakzent, für Labels)

**Typografie:**
- Überschriften/Marke: Source Serif 4 (seriös, kanzleihaft)
- Fließtext: Inter
- Bewusst KEINE Monospace-Schrift für Claims/Labels (frühere Idee, verworfen)

**Wichtige Entscheidungen, die im Designprozess gefallen sind:**
- KEINE Nummerierung (01/02/03 oder §1/§2/§3) bei der "Was Sie bekommen"- und "So funktioniert's"-Sektion — der Inhalt ist keine Sequenz, daher würde eine Nummerierung eine Reihenfolge behaupten, die nicht existiert. Stattdessen: dünne obere Trennlinie pro Kachel.
- Die drei Angebots-/Funktionspunkte sind bewusst kurz und ohne Fachbegriffe gehalten — Zielgruppe sind Handwerker, keine IT-affinen Leser.
- Mobile-Nav wird zum Hamburger-Menü, NICHT zu gestapelten Textlinks — hält den Header ruhig.

## Zielgruppe & Tonalität
Kleine Handwerksbetriebe (3–15 Mitarbeitende) und Hausverwaltungen, die noch mit Zetteln/Excel/WhatsApp arbeiten. Die meisten haben KEIN Microsoft 365 und sind nicht technikaffin. Tonalität: ruhig, konkret, ohne Anglizismen, ohne Buzzwords ("Digitalisierung", "Synergie" etc. vermeiden). Sätze kurz halten.

## Produkt-Kontext (für inhaltliche Änderungen relevant)
Das beworbene Angebot ("Erster Schritt Digital") ist eine bewusst sehr einfache Lösung:
- Tally.so-Formular (kostenlos) → automatische Google-Sheets-Anbindung (native Tally-Integration) → E-Mail-Benachrichtigung
- Bewusst KEIN Microsoft/Power Automate in dieser ersten Stufe — das kommt erst als möglicher späterer Ausbauschritt bei zufriedenen Kunden
- Preis: 299 € einmalige Einrichtung, 0 € laufende Kosten, kein Abo in dieser Phase

## Offene nächste Schritte
- [ ] Domain registrieren (z. B. canzler-digital.de)
- [ ] Cloudflare Pages mit diesem Repository verbinden
- [ ] Impressum- und Datenschutz-Seite ergänzen (Pflicht nach §5 TMG, in Deutschland gewerblich)
- [ ] Echte Kontakt-E-Mail-Adresse einsetzen (aktuell Platzhalter `hallo@canzler-digital.de`)
- [ ] Ggf. Open-Graph-Meta-Tags für Vorschaubilder beim Teilen ergänzen

## Deployment
- Lokales Git-Repository ist bereits eingerichtet.
- Erstellen Sie ein GitHub-Repository, z. B. `canzler-digital`, und verbinden Sie es mit dem lokalen Projekt:
  ```bash
git remote add origin https://github.com/<Ihr-Benutzername>/canzler-digital.git
git push -u origin master
```
- Erstellen Sie ein neues Cloudflare Pages Projekt und verbinden Sie es mit dem GitHub-Repository.
- Wählen Sie den Branch `master` oder `main` und setzen Sie das Build-Output-Verzeichnis auf `/`.
- Da die Seite aus reinem HTML/CSS besteht, ist kein Build-Befehl nötig.
- Die Seiten `impressum.html` und `datenschutz.html` sind bereits zum Repo hinzugefügt.
- Wenn eine eigene Domain registriert wird, kann sie anschließend in Cloudflare Pages als benutzerdefinierte Domain aktiviert werden.

## Hinweis für die Weiterarbeit
Der Eigentümer dieses Projekts ist nicht technisch versiert (kein Hosting-/Code-Hintergrund), aber klar in seinen Designentscheidungen — bitte Rückfragen stellen statt eigenständig vom Design-System abzuweichen, besonders beim Signatur-Lockup und der Farbpalette. Änderungswünsche kamen im bisherigen Prozess oft aus sehr genauem visuellem Hinsehen (z. B. Breitenverhältnis Logo/Claim, Mobile-Verhalten) — entsprechend sorgfältig prüfen, bevor Layoutänderungen vorgenommen werden.
