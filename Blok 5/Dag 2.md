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
Task kan return waarden heeft.
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

Meerdere tasks
```cs
Task[] tasks = new Task[] 
{ 
	Task.Run(() => DoSomething()),
	Task.Run(() => DoSomething2()), 
}; 
// Task.WaitAny(tasks);
// Task.WhenALl(tasks).ContinueWith(() => ..., TaskScheduler.FromCurrentSynchronizationContext());
Task.WaitAll(tasks, 5000); 
int numberOfFinishedTasks = Task.WaitAny(tasks, 10000);
```

