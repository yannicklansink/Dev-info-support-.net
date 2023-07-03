Kahoot quiz over git -> opsturen voor 10 uur naar email Nico
## Git
### git switch vs git checkout:
Met checkout kan je switchen, maar ook werk wat je lokaal hebt staan ongedaan maken.
git checkout -- features/ziekenhuis.md
Hetzelfde als git restore .
Dit checkout is oud en is een soort bug waar het voor 2 verschillende functionaliteiten zorgt.

### Git merge strategieen:
Git merge --squash branchname
git commit voordeel: lineaire geschiedenis en vaak netter.

Git commit

git tag v1.0 -> create new tag
git tag -> lijst met tags

### States of Tracking
untracked (nadat je een file toevoegt)
unmodified (na git commit) (zie je niet met git status)
modified (na het wijzigen van een file)
staged (als je git add .)

git diff:
zien wat je hebt toegevoegd.

git reset:
undo your code changes, om een fout op te lossen.
git reset hashcode
git reset HEAD~1 (vanaf je HEAD 1 commit terug)

git revert:
de betere reset

### .gitignore
Je wilt in je source control geen build output hebben staan.
Oplossing is door .gitignore file toe te voegen.
Gebruik github.com/github/gitignore

.gitkeep file:
Om lege folders toe te voegen aan git

### switch naar een vroegere commit
git switch --detach hashcode
Hierna moet je een branch maken, anders verlies je je werk als je aanpassingen doet.

-------------------------

## Docker

Open source, since 2014, build once, run everywhere.
Mogelijkheid voor maandelijkse abonnement.

### Container
- Isolated (bepaalde versie van db of dependencies)
	- Eigen file systems
	- Eigen processen
	- Eigen netwerk
	- Gereserveerde resources
- Standardized 
- Easy to deploy 

2 soorten containers:
- linux container (hier werkt de wereld mee)
- windows container

Docker Registry:
soort github voor docker images.
docker pull hello-world (will pull the image)

docker ps -a (om alle processen te zien)
docker images (om alle images te zien)
docker rm (om een proces of container weg te gooien)
docker rmi (om een image te verwijderen)

Je runt een container
Image is een blauwdruk om een container te runnen
Een instantie. Zelfde als een class en object.

### Docker ecosystem
docker compose (meerdere images aan elkaar koppellen)
ubuntu
kubernetes
trivy
snyk...

