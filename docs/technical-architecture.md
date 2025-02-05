# Technische Architectuur

De Softwarecatalogus is opgebouwd uit verschillende Common Ground componenten die samen een complete oplossing vormen. Hieronder volgt een overzicht van de belangrijkste componenten en hun functies.

![Component Diagram](diagrams/components.svg)

## Componenten

### Publicatie Voorziening (Frontend)
De frontend van de Softwarecatalogus wordt verzorgd door de Publicatie Voorziening. Deze component:
- Biedt een gebruiksvriendelijke interface voor eindgebruikers
- Zorgt voor een toegankelijke presentatie van de catalogusgegevens
- Implementeert de gebruikersinteractie en zoekfunctionaliteit
- Visualiseert GEMMA-views met ArchiMate symbolen
- Ondersteunt SVG export van architectuurviews
- Biedt interactieve definitieweergave (Glossary functionaliteit)

### Open Catalogi
Dit component is verantwoordelijk voor:
- Het inrichten van de catalogusstructuur
- Zoekfunctionaliteit en filtering
- Metadata management
- Categorisering en tagging van software
- GEMMA ArchiMate model importeren en verwerken
- Beheer van relaties tussen pakketten en GEMMA architectuur
- API voor GEMMA architectuurconcepten

### Open Registers
De datalaag wordt verzorgd door Open Registers, die:
- Fungeert als centrale dataopslag
- Beheert de basisregistraties van software en organisaties
- Zorgt voor data-integriteit en versioning
- Biedt een API voor data-toegang
- Slaat GEMMA architectuurconcepten op
- Beheert versies van het GEMMA ArchiMate model

### Open Connector
De Open Connector component:
- Verzamelt data uit externe bronnen (zoals CMDB's)
- Aggregeert en transformeert data naar het juiste formaat
- Synchroniseert data tussen verschillende systemen
- Implementeert de benodigde koppelingen met externe systemen
- Verzorgt AMEFF import/export functionaliteit
- Koppelt met GEMMA Online voor detailinformatie

## Referentiearchitectuur Functionaliteit

### ArchiMate Integratie
![ArchiMate Integration](diagrams/archimate_integration.svg)

De oplossing ondersteunt:
1. AMEFF bestandsimport (< 2 minuten voor 14MB)
2. Versie management van GEMMA modellen
3. Behoud van bestaande relaties bij updates
4. Automatische rollback bij importfouten
5. AMEFF export van pakketoverzichten en koppelingen.

### GEMMA Architectuur Ontsluiting
- JSON REST API voor GEMMA architectuurconcepten
- Zoek- en filterfunctionaliteit op archimate concepten 
- Linked Data API voor definities
- Directe koppelingen naar GEMMA Online
- Configureerbare basis-URLs voor verschillende omgevingen

### Visualisatie
- Interactieve GEMMA-views
- ArchiMate symbolenondersteuning
- SVG export functionaliteit
- Inzoombare views
- Hover-functionaliteit voor definities
- Consistente styling met GEMMA Online

## Interactie tussen Componenten

De componenten werken samen volgens Common Ground principes:
1. Data wordt bij de bron opgehaald
2. Componenten communiceren via gestandaardiseerde API's
3. Er is een duidelijke scheiding tussen data en functionaliteit

## GEMMA ArchiMate Model

De Softwarecatalogus maakt gebruik van het officiële GEMMA ArchiMate-model. Dit model is te vinden op de pagina [Download GEMMA ArchiMate-repository](https://www.gemmaonline.nl/index.php?title=Download_GEMMA_ArchiMate-repository). Hier de directe link naar het [GEMMA AMEFF bestand](https://github.com/VNG-Realisatie/GEMMA-Archi-repository/blob/master/export/GEMMA%20release.xml). Dit model:
- Is beschikbaar als AMEFF (ArchiMate Model Exchange File Format) export 
- Wordt regelmatig geactualiseerd en doorontwikkeld en gepubliceerd op github
- Bevat de complete GEMMA referentiearchitectuur
- Kan worden geïmporteerd in architectuurtools zoals Archi
- Onderzoekspuntje -> releasen vanaf github
- Het is bedoeling dat acceptatie op een andere versie van Gemma kan draaien dan Prod

### Ontwikkeltools
Voor het werken met ArchiMate modellen raden we de volgende tools aan:

#### Archi Tool
[Archi](https://www.archimatetool.com/) is een open source ArchiMate modelling tool die:
- Gratis te gebruiken is
- Beschikbaar is voor Windows, Mac en Linux
- AMEFF import/export ondersteunt
- Uitgebreide documentatie heeft
- Actief wordt onderhouden

Ga naar de GEMMA online pagina [ArchiMate modelleren](https://redactie.gemmaonline.nl/wiki/ArchiMate_modelleren) voor meer informatie en links.

#### GEMMA ArchiMate Repository
Het [GEMMA AMEFF bestand](https://github.com/VNG-Realisatie/GEMMA-Archi-repository/blob/master/export/GEMMA%20release.xml) kan worden gedownload om:
- De referentiearchitectuur te bestuderen
- De structuur van het AMEFF formaat te begrijpen
- Te testen met imports en exports
- Views en relaties te analyseren

Het model wordt gebruikt voor:
- Het importeren van nieuwe GEMMA releases
- Het koppelen van software aan referentiecomponenten
- Het exporteren van gemeentelijke architectuuroverzichten
- Het visualiseren van architectuurviews 
