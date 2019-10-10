---
author: Christian Erlinger
title: OPEN
subtitle:  Der Online-Katalog der Büchereien Wien
date: 2019-10-11
output:
  revealjs::revealjs_presentation:
    theme: sky
    css: style.css
---
### Systemarchitektur OPEN

![](open_sysarch.png)

### Neuerungen
* **Zeitgemäßere Web-Technologie** (Neuer Server, neue Software)
  * Responsives Design des Online-Kataloges
* **Integration der Website**
  * Open-Source CMS und kann/könnte individuell ergänzt werden.
* Integration der **Inhalte von Drittanbietern**:
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
  * Vergleich [StB Frankfurt](https://katalog.stadtbuecherei.frankfurt.de) - Suche Chaos Sys 5.1 und Nat 52
  * Vergleich [StB Salzburg](https://buch.stadt-salzburg.at/) - Suche nach "Engagement Hessel", Sys Gkk7, Gcx
  * Workaround über Systematiklink [buechereien.wien.gv.at/Mediensuche/Einfache-Suche?query=SC|SystematicLink|AND|2|Notation](https://buechereien.wien.gv.at/Mediensuche/Einfache-Suche?query=SC%7cSystematicLink%7cAnd%7c2%7cPL.MU)
  * Vertiefte Suche über Facettenfilter
* ~~Suche nach U-Sätzen in MBW~~


### Umgesetzte Korrekturen

* Stichwortsuche nach
  * Systematik
  * Erscheinungsjahr [Beispiel](https://buechereien.wien.gv.at/Mediensuche/Einfache-Suche?search=VS.IX+2019&top=y)
* Recherche mit Titel des MBW-H-Satzes liefert auch U-Sätze
  * Bsp: Briefmarkenband - [Michel Übersee Japan](https://buechereien.wien.gv.at/Mediensuche/Einfache-Suche?search=Michel+%C3%9Cbersee+Japan)

### Tricks bei der Recherche

* Trunkierung mit `*` funktioniert auch innerhalb eines Wortes
* Erweiterte Suche nach Systematik/Erscheinungsjahr im Feld "Stichwort"

### Bekannte Probleme #2

* Schlagwortfolgen: Verweisformen werden angezeigt
* Barrierefreiheit
* Indexierung der Mediensätze geht verloren
  * Bei Neuanlage eines Mediums überprüfen Sie doch bitte (sofern verfügbare Medien existieren), ob das Medium gefunden wird!
* Keine Phrasensuche möglich
* Keine Maskierung möglich

### Geplante Korrekturen

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

* [Buchwiki SoftwareTracking](https://www.intern.magwien.gv.at/buchwiki/user/bin/view/Tasks/SoWaTHome?Software=OPEN&Version=7.0&Alle=ja)
* [GitHub](https://github.com/bucwien)

