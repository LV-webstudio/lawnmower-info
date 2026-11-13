[English](README.md) · [Español](README.es.md) · **Français** · [Deutsch](README.de.md) · [Português](README.pt.md)

# Shania Lawnmower

> Une application de bureau Windows d’audit web intelligent : choisissez un site, un mode et lisez un rapport en langage clair.

![Shania Lawnmower](assets/banner.jpg)

*Bannière de marque Shania Lawnmower (illustration).*

## Ce que c’est

Shania Lawnmower est le visage de bureau du moteur d’analyse web de Shania. Vous choisissez une adresse web, un mode et un module ; l’application lance l’analyse et ouvre un rapport HTML qui explique chaque constat en langage clair : ce qui se passe, pourquoi c’est important, comment corriger et comment vérifier la correction. Elle propose des corrections mais ne modifie jamais votre site.

## Pour qui

- Petites entreprises et agences qui veulent savoir ce qui ne va pas sur leur site (en-têtes de sécurité, confidentialité, vitesse, accessibilité, SEO).
- Studios qui auditent leurs propres sites ou ceux de clients ayant donné leur accord.

## Ce que ça fait

- Modes d’analyse rapide et complet ; le complet ajoute Lighthouse (performance, SEO) et des contrôles d’accessibilité et nécessite Google Chrome.
- Mode passif (ce que voit tout visiteur) et mode autorisé pour vos domaines ou ceux autorisés, contrôlé par une liste blanche.
- Signaux publics sur la confidentialité et les cookies, les pages légales, les traceurs, les prestataires de paiement et les mentions de VeriFactu. Ce sont des indices, pas des certifications.
- Rapport de constats et plan de correction qui se contente de recommander ; il ne modifie ni fichiers ni site distant.
- Surveillance locale : répète l’analyse toutes les 24 heures tant que l’application est ouverte et compare les constats à la référence enregistrée.
- Un profil actif limité, bloqué sauf si un contrat signé, un périmètre défini et une revue professionnelle indépendante sont documentés. Ce n’est pas un test d’intrusion : aucune exploitation, force brute ni scan de ports.

## État

**En développement (MVP)**

L’application se compile en installateur Windows, mais l’installation sur un Windows vierge et un pilote sur des sites réels restent à faire. Pas encore proposée comme service aux clients. Nécessite Node.js 20 ou plus récent sur le PC.

## Le moteur : Analitics

Shania Lawnmower repose sur Analitics, le moteur d’analyse en ligne de commande de Shania Webstudio, qui peut aussi s’utiliser seul depuis un terminal (Node.js 20 ou plus récent).

- Domaines couverts : sécurité, confidentialité, performance, accessibilité, qualité et SEO. Chaque constat indique ce qui se passe, pourquoi c’est important, comment corriger, comment vérifier la correction, ainsi que le niveau de confiance de l’outil et la preuve.
- Avec l’option complète et Chrome installé : Lighthouse (médiane de trois passes par appareil) et contrôles d’accessibilité axe (WCAG A/AA).
- Collecteurs SEO et de préparation à l’IA (HTML, exploration, métadonnées) et une note globale avec des plafonds explicites pour les constats graves.
- Trois modes : passif (par défaut), autorisé (domaines de la liste blanche uniquement) et un profil actif limité, bloqué sans contrat, périmètre et revue professionnelle indépendante documentés.
- Des tests automatiques couvrent les options, les garde-fous d’autorisation, les erreurs des collecteurs et les rapports.
- Limites : c’est un outil local, pas un service d’audit déployable, et il ne certifie rien ; les contrôles juridiques, fiscaux et de paiement ne montrent que des signaux publics. Les transferts de données vers le W3C, Cloudflare et un dépôt public sont décrits plus bas.

## Données à connaître

Le validateur HTML reçoit le HTML de la page (W3C), les contrôles DNS utilisent le DNS sur HTTPS de Cloudflare et la liste des vulnérabilités de bibliothèques est téléchargée depuis un dépôt public. Ne l’utilisez pas sur des pages confidentielles sans vérifier ces transferts.

## À propos de ce dépôt

Ce dépôt ne contient que des informations : le code source est privé.

## Contact

- E-mail: hola@shaniawebstudio.com
- Site web: https://shaniawebstudio.com

---
*Un produit de Shania Webstudio.* · Copyright (c) 2026 Shania Webstudio.
