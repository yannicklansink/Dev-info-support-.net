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

Nadeel multithreading:
- Het kan 100.000 keer goed gaan, maar dan 1 keer fout. Moeilijk debuggen.
- Dit komt door gedeelte data tussen threads.

Stack bevat:
- Lokale variabelen
- Parameters
- Return adres
- Return value (functie die een waarde retourneert)

--------------------------------------

### Agenda
- Threads
- Tasks
- Async and await

I/O bound: Vaak aan het wachten op gebruikers. Threading helpt hierbij voor performance
CPU bound: Veel rekenwerk, de processor is nodig in volle capaciteit. Threading helpt niet hierbij voor performance

Why multithreading:
- More tasks than cores -> threading for scheduling
- More cores than tasks -> threading for parallelism (voor het trainen van een AI bijv.)

### .NET thread is een class
- thread class creates a windows thread when using start()
Properties in thread class:
- Name
- Property (je kan thread andere prioriteit geven om het belang aan te geven per thread)
- IsBackground
- IsThreadPoolThread
- ManagedThreadId
- ThreadState
Methodes
- Start()
- Join()
- Abort() (Nooit gebruiken, want thread is bezig met data. Data krijg je daardoor niet meer in geldige toestand)
- Interrupt() (Soort eindigen, betere manier. Zorgt voor een exception in the thread)

```cs
Object x = new Object();
lock(x) 
{
	// execute statements in lock
}
```

### .NET class BackgroundWorker
Voor situaties als je dingen op de achtergrond wilt runnen. Resultaat wordt in Result property gezet.
3 Events:
- DoWork
- ProgressChanged
- RunWorkerCompleted