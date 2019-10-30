# Installatie GOST Server

De Geodan GOST Server is een implementatie van de SensorThingsAPI in de programmeertaal Go.
Installatie gebeurt bij voorkeur met Docker. Dit kan met standaard Docker commando's, maar bij voorkeur
met `docker-compose` of zelfs in Kubernetes.

Het beste is om een van de [GOST Tutorials](https://www.gostserver.xyz/tutorials/) te volgen.

Hieronder worden een aantal methoden/ervaringen beschreven voor GOST installatie 
zoals tijdens de STA Hackathon 2019 ontwikkeld.

## Complete GOST Stack op Ubuntu
[Just van den Broecke](https://github.com/justb4/) beschrijft de installatie
van een complete GOST Stack op een leeg/nieuw Linux Ubuntu systeem op: https://github.com/justb4/stademo.

Deze inrichting is gebruikt voor de STA GOST demo server gebruikt in de hackathon: 

* GOST STA API Endpoint: https://sta.map5.nl/gost/v1.0/

(Overige URLs op aanvraag).

Dit betreft een aantal stappen:

* inrichten/beveiligen Ubuntu met Ansible
* GOST Stack deployen met `docker-compose` via Bash script

De GOST Stack bestaat uit:

* GOST Server, Postgres Server, Mosquitto MQTT Server Broker
* NodeRed IoT mapper
* Proxy front-end en SSL (via Let's Encrypt) met Traefik

Op een leeg Ubuntu systeem kan deze volledige installatie in plm 15 minuten.

## GOST op Kubernetes 
De deployment van GOST op K8S gerealiseerd in de 
hackathon door Kadaster/PDOK kan worden gevonden 
op: https://github.com/arbakker/sensor-things-hackathon-19
  
## GOST Links

* homepage: https://www.gostserver.xyz/
* overzicht links: https://github.com/gost/home
* GitHub: https://github.com/gost
* Docker Images: https://hub.docker.com/r/geodan/gost/

 