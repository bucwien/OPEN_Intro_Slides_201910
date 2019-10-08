---
author: Christian Erlinger
title: OPEN
subtitle:  Der Online-Katalog der Büchereien Wien
date: 2019-10-08
output:
  revealjs::revealjs_presentation:
    theme: sky
    css: style.css
---
### Systemarchitektur OPEN

![](open_sysarch.png)

### Neuerungen
* Zeitgemäße Web-Technologie (Neuer Server, neue Software)
  * Responsives Design des Online-Kataloges
* Integration der Website
  * OPEN läuft in einem Open-Source CMS und kann somit (tlw.) ergänzt werden.
* Bessere Integration Inhalte von Drittanbietern:
  * Verfügbarkeitsanzeige bei E-Medien der Onleihe (theoretisch)
  * Cover-Abbildungen

### Neuerungen - Suche

* Suche in Solr-Index anstatt direkt in der Datenbank
  * Autovervollständigung während der Suchbegriffseingabe
  * Facettierung und Filterung der Suchergebnisse
  * „Meinten Sie“-Vorschlag
  * Suche schneller als in relationaler Datenbank
* Features für BenutzerInnen:
  * Medienmerkliste, Suchen speicherbar
  * Direkte Vormerkung am spezifischen Exemplar

### Bekannte Probleme #1

* Erweiterte Suche: Systematik/IKA (deaktiviert)
  * Workaround über Systematiklink [buechereien.wien.gv.at/Mediensuche/Einfache-Suche?query=SC|SystematicLink|AND|2|Notation](https://buechereien.wien.gv.at/Mediensuche/Einfache-Suche?query=SC%7cSystematicLink%7cAnd%7c2%7cPL.MU)
  * Vertiefte Suche über Facettenfilter
* Suche nach U-Sätzen in MBW:
  * Briefmarkenbeispiel: Michel Übersee - Bd. 9.2 Japan
  * Workaround auf [QM](https://openm13.wien.gv.at/Mediensuche/Einfache-Suche?search=Michel+%C3%9Cbersee+Japan) implementiert (MBW-Titel wird als Reihentitel indexiert)

### Bekannte Probleme #2

* Schlagwortfolgen: Verweisformen werden angezeigt
* Barrierefreiheit

### Geplante Korrekturen

* Stichwortsuche ergänzen um Jahr und Systematik
* Systematik-Register
* Verlinkung der Standort-Angaben
* **!! Metadaten-Korrekturen !!**
  * Sprachen-Facette (Datenbereinigung)
  * Sys-/IKA-Facette (aufwändige Datenbereinigung nötig)
  * Schlagwortregister bereinigen (GND-Verlinkung herstellen)

### Träume möglich

* Erweiterte Suche selbst aufbauen 
  * Semantische Suche erlauben ([Siehe](https://nbn-resolving.org/urn:nbn:de:0290-opus4-162355))
* Dynamische Medienvorschläge (Festtage, Jubiläen, aktuelle Ereignisse)
* Kuratierte Liste einbetten (zB dynamische Liste an Literaturpreis-TrägerInnen)
* Zeitschriftenartikel indexieren
* *...und?*

### Error Reporting

* [Buchwiki SoftwareTracking](https://www.intern.magwien.gv.at/buchwiki/user/bin/view/Tasks/SoWaTHome?Software=Teststellung%20Open&Version=7.0&Alle=ja)
* [GitHub](https://github.com/bucwien)

### Outcomes Besprechung 03.10.2019

[Dokumentiert](https://github.com/buechereien-wien/OPEN_Intro_Slides_201910/issues/8)

* Systematik-Notationen in `DefaultSearchField` kopieren
* Erscheinungsjahr in `DefaultSearchField` kopieren

* Bei **OCLC** melden:
  * Phrasensuche

### Frage/Anregung

Kollaborative Entwicklung von Beispielen oder Unterlagen zur Katalog-Recherche in OPEN

* Buchwiki
* oder auf GitHub als Slide-Show (wie diese hier) und gleichzeitig als [OER](https://de.wikipedia.org/wiki/Open_Educational_Resources) veröffentlichen?
