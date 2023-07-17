### Virtual Memory:
Als een proces wordt gestart krijgt het een stuk VM, waarvan het adres wordt geconverteerd naar een fysiek adres om een stuk geheugen te reserveren. 4K.

Een proces heeft geen invloed op andere processen.

### Context switch:
Wissel tussen de processen. Dit is duur. Door threading hoeft er geen context switch worden gedaan. 

### Threads:
Thread kunnen met elkaar communiceren en hebben hetzelfde adres.
Hebben dezelfde heap, maar eigen stack.

### Pagen:
Het wegschrijven van interne geheugen naar de harde schijf, om plek vrij te maken voor nieuwe processen. Dit gebeurt veel als je weinig RAM hebt. 

### Proces bestaat uit 4 onderdelen:
- Code.exe (dll) (RO)
	- Het eerste wat gebeurt van een proces is het inladen van de code.
- Data (R/W)
	- Globaal geheugen
	- Stack geheugen
	- Heap geheugen
- Registers
	- Zit op de processor (cpu)
	- Soort werkgeheugen van de processor
	- Program Counter (PC) -> wijst naar de volgende instructie. Pointer. (thread zorgt voor extra PC)
	- Stack Pointer (SP) -> wijst naar de stack. (thread zorgt voor extra SP)
- Resources
	- Externe dingen die je gebruikt. Bijv. een file die je opent.

