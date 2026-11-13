[English](README.md) · [Español](README.es.md) · [Français](README.fr.md) · **Deutsch** · [Português](README.pt.md)

# Shania Lawnmower

> Eine Windows-Desktop-App für intelligentes Website-Auditing: Seite wählen, Modus wählen, Bericht in klarer Sprache lesen.

![Shania Lawnmower](assets/banner.jpg)

*Markenbanner von Shania Lawnmower (Grafik).*

## Was es ist

Shania Lawnmower ist das Desktop-Gesicht der Website-Analyse-Engine von Shania. Du wählst eine Webadresse, einen Modus und ein Modul; die App führt die Analyse aus und öffnet einen HTML-Bericht, der jeden Befund verständlich erklärt: was passiert, warum es wichtig ist, wie man es behebt und wie man die Behebung prüft. Sie schlägt Korrekturen vor, ändert aber nie deine Website.

## Für wen

- Kleine Unternehmen und Agenturen, die wissen wollen, was an ihrer Website nicht stimmt (Sicherheits-Header, Datenschutz, Geschwindigkeit, Barrierefreiheit, SEO).
- Studios, die eigene Websites oder die von Kunden mit Erlaubnis prüfen.

## Was es kann

- Schneller und vollständiger Analysemodus; der vollständige ergänzt Lighthouse (Leistung, SEO) und Barrierefreiheitsprüfungen und benötigt installiertes Google Chrome.
- Passiver Modus (was jeder Besucher sieht) und autorisierter Modus für eigene oder freigegebene Domains, gesteuert über eine Positivliste.
- Öffentliche Signale zu Datenschutz und Cookies, Rechtsseiten, Trackern, Zahlungsanbietern und VeriFactu-Erwähnungen. Das sind Hinweise, keine Zertifizierungen.
- Bericht mit Befunden und Korrekturplan, der nur empfiehlt; Dateien oder die Live-Website werden nicht verändert.
- Lokale Überwachung: wiederholt die Analyse alle 24 Stunden, solange die App geöffnet ist, und vergleicht die Befunde mit dem gespeicherten Referenzstand.
- Ein eingeschränktes aktives Profil, das gesperrt bleibt, solange kein unterzeichneter Vertrag, kein definierter Umfang und keine unabhängige fachliche Prüfung dokumentiert sind. Es ist kein Penetrationstest und führt keine Ausnutzung, Brute-Force- oder Portscans durch.

## Status

**In Entwicklung (MVP)**

Die App wird als Windows-Installer gebaut; die Installation auf einem sauberen Windows-Rechner und ein Pilot mit echten Websites stehen noch aus. Noch nicht als Dienst für Kunden angeboten. Erfordert Node.js 20 oder neuer auf dem PC.

## Die Engine: Analitics

Shania Lawnmower läuft auf Analitics, der Kommandozeilen-Analyse-Engine von Shania Webstudio, die sich auch allein über ein Terminal nutzen lässt (Node.js 20 oder neuer).

- Abgedeckte Bereiche: Sicherheit, Datenschutz, Leistung, Barrierefreiheit, Qualität und SEO. Jeder Befund sagt, was passiert, warum es wichtig ist, wie man es behebt, wie man die Behebung prüft und wie sicher das Werkzeug ist und auf welcher Evidenz.
- Mit der Volloption und installiertem Chrome: Lighthouse (Median aus drei Durchläufen je Gerät) und axe-Barrierefreiheitsprüfungen (WCAG A/AA).
- SEO- und KI-Readiness-Collector (HTML, Crawling, Metadaten) sowie eine Gesamtbewertung mit ausdrücklichen Obergrenzen bei schweren Befunden.
- Drei Modi: passiv (Standard), autorisiert (nur Domains der Positivliste) und ein eingeschränktes aktives Profil, das ohne dokumentierten Vertrag, Umfang und unabhängige fachliche Prüfung gesperrt bleibt.
- Automatische Tests decken die Optionen, die Autorisierungssperren, Collector-Fehler und die Berichte ab.
- Grenzen: Es ist ein lokales Werkzeug, kein einsetzbarer Audit-Dienst, und es zertifiziert nichts; rechtliche, steuerliche und Zahlungsprüfungen zeigen nur öffentliche Signale. Die Datenübertragungen an W3C, Cloudflare und ein öffentliches Repository werden weiter unten beschrieben.

## Wichtig zu wissen: Datenübertragungen

Der HTML-Validator erhält den HTML-Code der Seite (W3C), die DNS-Prüfungen nutzen Cloudflare DNS-over-HTTPS und die Liste bekannter Bibliotheks-Schwachstellen wird aus einem öffentlichen Repository geladen. Nicht für vertrauliche Seiten verwenden, ohne diese Übertragungen zu prüfen.

## Über dieses Repository

Dieses Repository enthält nur Informationen: Der Quellcode ist privat.

## Kontakt

- E-Mail: hola@shaniawebstudio.com
- Website: https://shaniawebstudio.com

---
*Ein Produkt von Shania Webstudio.* · Copyright (c) 2026 Shania Webstudio.
