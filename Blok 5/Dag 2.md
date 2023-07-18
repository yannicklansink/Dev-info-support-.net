Zodra je met lambdas werkt met locale variabelen moet je uitkijken wat je doet. Variabelen gaan dan naar de heap.

### Threadpool
- Teveel threads verminderen de performance
- Beste om 1 thread per core
	-  Oplossing => threadpool
- Creeer niet je eigen thread, maar stuur het naar de threadpool
	- ThreadPool.QueueUserWorkItem(o => );


### Task Parallel Library (TPL)
- Extension voor de ThreadPool
- Welke taken maak je aan.
- Task kunnen worden gebruiken:
	- Explicit en Implicit

### Task
```cs
Task task = new Task(
	() =>
	{
		Console.WriteLine("Working");
	}
);
task.Start();
```