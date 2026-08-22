# Aufenthaltsorte der Artist:innen und Geschäftsorte der Künstleragenturen in der Zeitschrift "Organ" (Warschau)

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![License: MIT](https://img.shields.io/badge/Code_License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

## Über das Projekt

Dieses Repository enthält den Workflow und die Skripte zur Extraktion, Aufbereitung und Georeferenzierung historischer Ortsdaten aus der Zeitschrift **Organ** (Warschau 1910-1915). 

---

## Methodik & Data Provenance

Die Datenverarbeitung gliedert sich in folgende Schritte:

1. **Texterfassung (OCR):** Extraktion der Textdaten aus digitalisierten Ausgaben der Zeitschrift. Organ (Warschau), Nr. 23, 01.12.1910; Nr. 104,         11.01.1914.
2. **Datenbereinigung:** Bereinigung von OCR-Fehlern, Standardisierung der Formate und Strukturierung der Ortsnennungen.
3. **Historische Georeferenzierung:**
   - Manuelle und automatisierte Recherche historischer Ortsbezeichnungen und Toponyme.
   - Zuordnung von Geokoordinaten (Breiten- und Längengrade).
4. **GIS-Verarbeitung & Harmonisierung (R):**
   - Extraktion historischer Grenzverläufe aus dem R-Package [`cshapes`](https://cran.r-project.org/package=cshapes).
   - Abfrage und Import ergänzender historischer Shapefiles/Vektordaten aus **OpenHistoricalMap (OHM)** via **Overpass API** (Overpass Turbo).
   - Abgleich und Angleichung der Kartendaten an die Vektordaten von **HistoGIS** (*Austrian Centre for Digital Humanities and Cultural Heritage /         ÖAW*).
5. **Interaktive Visualisierung (Leaflet):** Aufbereitung der harmonisierten Geodaten für eine interaktive Kartendarstellung im Web mittels des R-Pakets `leaflet` (bzw. JavaScript Leaflet.js).
6. **Code-Generierung & AI Transparency:** Der Code für die Datenverarbeitung in R sowie die Erstellung der Leaflet-Karte wurde unter Einsatz von KI-Assistenz generiert, angepasst und validiert.

