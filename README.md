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

## Beveiliging
SensorthingsAPI zegt zelf niets over beveiliging. Het is voor gebruik van de overheid wel belangrijk om te weten dat sensorgegevens onveranderd van sensor naar server getransporteerd kunnen worden (integriteit), dat onbevoegde er niet bij kunnen in het geval van gevoelige data (toegang). Dat informatie echt van de sensor komt (auhtentieke bron). Een Nederlands profiel kan uitspraken doen over hoe deze vraagstukken op te lossen met bestaande andere standaarden. 

