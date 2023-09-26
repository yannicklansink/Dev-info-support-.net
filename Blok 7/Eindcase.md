Garage administratiesysteem.

Onderhoudsformulier moet digitaal.
Factuur moet digitaal en mailen naar de krant.

Monteurs moeten in het systeem. 
Receptionist moet in het systeem.
Admin moet in het systeem.

RDW op te hoogte houden. RDW wilt weten of de auto goed gekeurd is. Check doen bij RDW. XML bestand staat of de auto moet worden gecontroleerd. 

Klant op hoogte houden wanneer; (via telefoon)
- Steekproef (controle RDW)
- Duurder uitvalt
- Klaar is voor ophalen

Entiteiten:
- Werknemer (monteur, receptionist, admin)
- Auto
- Onderhoudsformulier
- Klant
- Product(prijs= kan zijn dat het onbekend is)
- Factuur

Admin moet:
- facturen CRUD


Docker container van RDW.



### To run project locally:

dotnet publish --configuration Release
docker build -t my-backend .

docker build -t yannicklansink/av-app-image

docker login kcbdregistry.azurecr.io --username b908d8bd-293d-4506-ab4b-cb3b4de16d1b --password WYd8Q~tGhWEZhErK8hGaOj8Gv4EXUD-5MhM~xbBN

docker-compose up --build -d



