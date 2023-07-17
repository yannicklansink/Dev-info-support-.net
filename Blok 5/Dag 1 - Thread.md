### Virtual Memory:
Als een proces wordt gestart krijgt het een stuk VM, waarvan het adres wordt geconverteerd naar een fysiek adres om een stuk geheugen te reserveren. 4K.

Een proces heeft geen invloed op andere processen.

### Context switch:
Wissel tussen de processen. Dit is duur. Door threading hoeft er geen context switch worden gedaan. 

### Threads:
Thread kunnen met elkaar communiceren en hebben hetzelfde adres.

### Pagen:
Het wegschrijven van interne geheugen naar de harde schijf, om plek vrij te maken voor nieuwe processen. Dit gebeurt veel als je weinig RAM hebt. 

### Proces bestaat uit 4 onderdelen:
- Code.exe (dll) (RO)
	- Het eerste wat gebeurt van een proces is het inladen van de code.
- Data (R/W)
	- Globaal geheugen
	- Stack geheugen
	- Heap geheugen

