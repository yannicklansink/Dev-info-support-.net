
### Vormen van isoleren:
- Multi threading:
Hebben meerdere threads, en dus meerdere stacks. Ze maken gebruik van 1 heap.
Stack is geisoleerd
- Multi Proces:
Meerdere apps laten runnen.
- Containerization:
Operating system feature
- Virtualization:
Werd in het verleden gedaan. 
- Hardware:
Dan zet je 2 computers naast elkaar...


### Volumes
Docker-volumes zijn een mechanisme om gegevens die door Docker-containers worden gegenereerd en gebruikt, te behouden.
Om vanuit 2 containers 1 local file uit te lezen. Gegevens staan los van de docker levenscyclus.
`docker volume create volume-name`


### Docker Hub
De github voor docker
docker build -t (username)/

`yannicklansink/unbuntu:latest`
yannick lansink: points to the repository
unbuntu: points to the image
latest: is the standard tag

### Docker Compose
Docker Compose is een tool voor het definiëren en beheren van multi-container Docker applicaties. Het gebruikt YAML bestanden om de services van je applicatie te configureren en stelt je in staat om al deze services tegelijkertijd te creëren en te beheren.

Met Docker Compose kun je met één enkel commando je gehele app-omgeving starten, stoppen en opnieuw bouwen.

docker-compose.yml
`docker compose up` is een soort docker run
`docker compose down` is een soort docker stop en remove in een


### Commands:
```bash 
#dotnet publish --configuration Release
#docker build -t todo .
#docker network create todonetwork
#docker run -h sql --network todonetwork -e "ACCEPT_EULA=Y" -e 'MSSQL_SA_PASSWORD=MyL1ttlePony123!!' -p 1433:1433 -d --name sql-todo mcr.microsoft.com/mssql/server:2022-latest 
#docker run --name todo-app --network todonetwork -p 5001:80 -e 'ConnectionStrings__TodoContext=Server=sql; Database=tododb; User=sa; Password=MyL1ttlePony123!!; TrustServerCertificate=true;' todo
```

-d == deamon

dotnet  public -c Release (om het opnieuw te compileren)
docker compose up --build (om een dotnet app opnieuw te runnen en builden)