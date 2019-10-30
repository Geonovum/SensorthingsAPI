# SensorthingsAPI
repo voor de SensorthingsAPI hackathon
Je vindt hier gedeelde kennis en voorbeeld (sensor)data die tijdens de hackathon gebruikt worden

# Sensordata grondwaterstanden
De sensor data voor grondwaterstanden die [hier](https://github.com/Geonovum/SensorthingsAPI/tree/master/voorbeeld%20data%20grondwaterstanden) wordt aangeboden is bedoeld als voorbeelddata om tijdens de hackathon te gebruiken. De data komt met geen enkele garantie. De data is dus zeker niet volledig en ook de nauwkeurigheid en correctheid is niet gegarandeerd.
# K8S GOST
De deployment van GOST op K8S gerealiseerd in de hackathon kan worden gevonden op: https://github.com/arbakker/sensor-things-hackathon-19 

# Aandachtspunten Nederlands profiel sensorthingsAPI
## Ruwe data inwinnen & uitleveren
Sensorthings lijkt heel geschikt voor het standaardiseerd verzamelen en uitgeven van "ruwe" sensordata.
## Analyses
Sensorthings biedt uitgebreide mogelijkheden om verschillende soorten filtering toe te passen en daarmee analyses te doen. Is het handig om gebruik van SensorthingsAPI hiervoor te verplichten?
## Aansluiten op OAS (open API specificatie)
Het is niet mogelijk om de volledige functionaliteit van sensorthingsAPI uit te drukken in OAS (swagger). OAS is wel een standaard op de Pas Toe of leg Uit lijst van het forum standaardisatie. Het zou handig zijn om richting te geven hoe je om kan gaan met het gebruik van OAS. Zelfs wanneer het niet de hele API kan beschrijven zou het behulpzaam kunnen zijn om een nieuwe gebruiker wegwijs te maken.
OASIS heeft een mapping van ODATA naar OAS: https://docs.oasis-open.org/odata/odata-openapi/v1.0/cn01/odata-openapi-v1.0-cn01.html
Een incomplete OAS specificatie kan hier gevonden worden: https://github.com/Glagnar/OGCSensorThings/blob/master/Swagger-Source/cloud-api.json
Wanneer je OAS wil gebruiken voor code generatie kan je ook gebruik maken van onderstaande tabel van Hylke van der Schaaf van Fraunhofer:
My path-counting-table (may contain errors):

	Count	Total
Path type |	STA v1.1 |	+MultiDS |	STA v1.1 |	MultiDS
--------------------------------------------------------
/v1.1	| 1 |	1 |	1	| 1
--------------------------------------------------------
/v1.1/Collection |	8	| 9 |	9 |	10
---------------------------------------------------------
/v1.1/Collection(entityId) |	8	| 9	| 17	| 19
-------------------------------------------------------------
/v1.1/Collection(entityId)/Relation | 	16	| 24	| 33	| 43
---------------------------------------------------------------------
/v1.1/Collection(entityId)/property |	37	| 46	| 70	| 89
--------------------------------------------------------------------
/v1.1/Collection(entityId)/property/$value |	37	| 46	| 107	| 135
-------------------------------------------------------------------------------
/v1.1/Collection/$ref |	8	| 9	| 115	| 144
------------------------------------------------------
/v1.1/Collection(entityId)/Relation/$ref |	10	| 15	| 125	| 159
--------------------------------------------------------------------------------
/v1.1/Collection(entityId)/Relation/property	| 29	| 46	| 154 |	205
----------------------------------------------------------------------------
/v1.1/Collection(entityId)/Relation/property/$value	| 29	| 46 |	183	| 251
-------------------------------------------------------------------------------------
/v1.1/Collection(entityId)/Relation/Relation	| 13	| 19	| 196 |	270
----------------------------------------------------------------------------
/v1.1/Collection(entityId)/Relation/Relation/$ref	| 10	| 14	| 206	| 284
-------------------------------------------------------------------------------------
/v1.1/Collection(entityId)/Relation/Relation/property |	12	| 20	| 218	| 304
--------------------------------------------------------------------------------------
/v1.1/Collection(entityId)/Relation/Relation/property/$value |	12	| 20	| 230	| 324
----------------------------------------------------------------------------------------------
/v1.1/Collection(entityId)/Relation/Relation/Relation |	5	| 9	| 235 |	333
----------------------------------------------------------------------------------
/v1.1/Collection(entityId)/Relation/Relation/Relation/$ref |	5 |	9	| 240 |	342
-------------------------------------------------------------------------------------------
/v1.1/Collection(entityId)/property/sub/property |	∞ |	∞+	| ∞	| ∞+
----------------------------------------------------------------------------------------
/v1.1/Collection(entityId)/property/sub/property/$value |	∞+	| ∞++ |	∞+	| ∞++
-----------------------------------------------------------------------------------------------
/v1.1/Collection(entityId)/Relation(entityId)/Relation(entityId)/…	| ∞++ |	∞+++ |	∞++ |	∞+++
------------------------------------------------------------------------------------------------


## Beveiliging
SensorthingsAPI zegt zelf niets over beveiliging. Het is voor gebruik van de overheid wel belangrijk om te weten dat sensorgegevens onveranderd van sensor naar server getransporteerd kunnen worden (integriteit), dat onbevoegde er niet bij kunnen in het geval van gevoelige data (toegang). Dat informatie echt van de sensor komt (auhtentieke bron). Een Nederlands profiel kan uitspraken doen over hoe deze vraagstukken op te lossen met bestaande andere standaarden. 

