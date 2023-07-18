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
Task<int> task = new Task<int>(() =>
	{
		Console.WriteLine("Working");
		return 42;
	}
);
task.Start();

Console.WriteLine(task.Result);
```

Task kan return waarden heeft.

