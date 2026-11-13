[English](README.md) · **Español** · [Français](README.fr.md) · [Deutsch](README.de.md) · [Português](README.pt.md)

# Shania Lawnmower

> Una aplicación de escritorio para Windows de auditoría web inteligente: eliges un sitio, un modo y lees un informe en lenguaje claro.

![Shania Lawnmower](assets/banner.jpg)

*Banner de marca de Shania Lawnmower (ilustración).*

## Qué es

Shania Lawnmower es la cara de escritorio del motor de análisis web de Shania. Eliges una dirección web, un modo y un módulo, y la aplicación ejecuta el análisis y abre un informe HTML que explica cada hallazgo en lenguaje claro: qué pasa, por qué importa, cómo arreglarlo y cómo comprobar el arreglo. Propone correcciones, pero nunca cambia tu sitio.

## Para quién

- Pequeñas empresas y agencias que quieren saber qué falla en su web (cabeceras de seguridad, privacidad, velocidad, accesibilidad, SEO).
- Estudios que auditan sus propias webs o las de clientes que han dado permiso.

## Qué hace

- Modos de análisis rápido y completo; el completo añade Lighthouse (rendimiento, SEO) y comprobaciones de accesibilidad, y necesita Google Chrome instalado.
- Modo pasivo (lo que ve cualquier visitante) y modo autorizado para dominios propios o con permiso, controlado por una lista blanca.
- Señales públicas sobre privacidad y cookies, páginas legales, rastreadores, proveedores de pago y menciones de VeriFactu. Son indicios, no certificaciones.
- Informe de hallazgos y plan de corrección que solo recomienda; no modifica archivos ni el sitio remoto.
- Monitorización local: repite el análisis cada 24 horas mientras la aplicación está abierta y compara los hallazgos con la referencia guardada.
- Un perfil activo limitado que queda bloqueado salvo que haya contrato firmado, alcance definido y revisión profesional independiente documentados. No es una prueba de penetración y no hace explotación, fuerza bruta ni escaneo de puertos.

## Estado

**En desarrollo (MVP)**

La aplicación se compila como instalador de Windows, pero siguen pendientes la instalación en un Windows limpio y un piloto con webs reales. Todavía no se ofrece como servicio a clientes. Requiere Node.js 20 o superior en el PC.

## El motor: Analitics

Shania Lawnmower funciona sobre Analitics, el motor de análisis de línea de órdenes de Shania Webstudio, que también puede usarse por separado desde una terminal (Node.js 20 o superior).

- Áreas que cubre: seguridad, privacidad, rendimiento, accesibilidad, calidad y SEO. Cada hallazgo dice qué pasa, por qué importa, cómo arreglarlo, cómo comprobar el arreglo y con qué confianza y evidencia lo afirma la herramienta.
- Con la opción completa y Chrome instalado: Lighthouse (mediana de tres pasadas por dispositivo) y comprobaciones de accesibilidad con axe (WCAG A/AA).
- Colectores de SEO y de preparación para IA (HTML, rastreo, metadatos) y una puntuación global con topes explícitos para los hallazgos graves.
- Tres modos: pasivo (por defecto), autorizado (solo dominios de la lista blanca) y un perfil activo limitado que queda bloqueado sin contrato, alcance y revisión profesional independiente documentados.
- Las pruebas automáticas cubren las opciones, las guardas de autorización, los errores de los colectores y los informes.
- Límites: es una herramienta local, no un servicio de auditoría desplegable, y no certifica nada; las comprobaciones legales, fiscales y de pagos solo muestran señales públicas. Las transferencias de datos al W3C, a Cloudflare y a un repositorio público se describen más abajo.

## Datos que conviene conocer

El validador de HTML recibe el HTML de la página (W3C), las comprobaciones DNS usan DNS sobre HTTPS de Cloudflare y la lista de vulnerabilidades de librerías se descarga de un repositorio público. No la uses en páginas confidenciales sin revisar antes estas transferencias.

## Sobre este repositorio

Este repositorio solo contiene información: el código es privado.

## Contacto

- Correo: hola@shaniawebstudio.com
- Web: https://shaniawebstudio.com

---
*Un producto de Shania Webstudio.* · Copyright (c) 2026 Shania Webstudio.
