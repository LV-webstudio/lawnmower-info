# Shania Lawnmower — website audit app for SEO, security and accessibility

> A Windows desktop app for intelligent website auditing: pick a site, pick a mode, read a plain-language report.

By [Shania Webstudio](https://shaniawebstudio.com), Granada (Spain).

**English** · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Português](README.pt.md)

![Shania Lawnmower](assets/banner.jpg)

*Shania Lawnmower brand banner (artwork).*

## What it is

Shania Lawnmower is the desktop face of the Shania website analysis engine. You choose a web address, a mode and a module, and the app runs the analysis and opens an HTML report that explains each finding in plain language: what happens, why it matters, how to fix it and how to check the fix. It proposes corrections but never changes your site.

## Who it is for

- Small businesses and agencies that want to know what is wrong with their website (security headers, privacy, speed, accessibility, SEO).
- Studios that audit their own sites or those of clients who have given permission.

## What it does

- Quick and full analysis modes; the full mode adds Lighthouse (performance, SEO) and accessibility checks and needs Google Chrome installed.
- Passive mode (what any visitor can see) and an authorised mode for your own or permitted domains, controlled by an allow-list.
- Public signals on privacy and cookies, legal pages, trackers, payment providers and VeriFactu mentions. These are indications, not certifications.
- Report of findings and a correction plan that only recommends; it does not modify files or the remote site.
- Local monitoring: repeats the analysis every 24 hours while the app is open and compares findings with the saved baseline.
- A limited active profile that is blocked unless a signed contract, a defined scope and an independent professional review are documented. It is not a penetration test and performs no exploitation, brute force or port scanning.

## Status

**In development (MVP)**

The app builds as a Windows installer, but installation on a clean Windows machine and a pilot on real sites are still pending. Not yet offered as a service to clients. Requires Node.js 20 or newer on the PC.

## The engine: Analitics

Shania Lawnmower runs on Analitics, the command-line analysis engine of Shania Webstudio, which can also be used on its own from a terminal (Node.js 20 or newer).

- Areas covered: security, privacy, performance, accessibility, quality and SEO. Each finding states what happens, why it matters, how to fix it, how to verify the fix, and how confident the tool is and on what evidence.
- With the full option and an installed Chrome: Lighthouse (median of three passes per device) and axe accessibility checks (WCAG A/AA).
- SEO and AI-readiness collectors (HTML, crawling, metadata) and an overall score with explicit caps for serious findings.
- Three modes: passive (default), authorised (allow-listed domains only) and a limited active profile that stays blocked without documented contract, scope and independent professional review.
- Automated tests cover the options, the authorisation guards, collector errors and the reports.
- Limits: it is a local tool, not a deployable audit service, and it certifies nothing; legal, tax and payment checks only show public signals. The data transfers to W3C, Cloudflare and a public repository are described below.

## Data you should know about

The HTML validator receives the page HTML (W3C), DNS checks use Cloudflare DNS-over-HTTPS and the library vulnerability list is downloaded from a public repository. Do not use it on confidential pages without reviewing these transfers.

## About this repository

This repository contains information only: the source code is private.

## Contact

- Email: hola@shaniawebstudio.com
- Website: https://shaniawebstudio.com

---
*A product by Shania Webstudio.* · Copyright (c) 2026 Shania Webstudio.
