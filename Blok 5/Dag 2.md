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

1. `Interlocked.Add(ref totalResult, result);`
    
    This line atomically adds the value of `result` to `totalResult`. In other words, it ensures that the operation (`totalResult += result`) is completed in an atomic manner. This means that once a thread starts this operation, no other thread can interrupt it until it's finished. This is important in a multi-threaded environment, as without atomic operations, one thread could read the value of `totalResult`, then another thread could change `totalResult`, and then the first thread could write back the old value it read plus `result`, thereby disregarding the change made by the second thread. This scenario is known as a race condition.
    
2. `int calculatedCount = Interlocked.Increment(ref numberOfCalculations);`
    
    This line atomically increments the value of `numberOfCalculations` by one. It's similar to writing `numberOfCalculations++`, but `Interlocked.Increment` ensures that the operation is completed atomically. This is necessary to prevent the same kind of race condition that I explained above. If two threads simultaneously read the value of `numberOfCalculations`, increment it, and write it back, the value could end up being incremented by one instead of two.

`TaskScheduler.FromCurrentSynchronizationContext()` returns a `TaskScheduler` that targets the synchronization context of the UI thread. This allows tasks to be scheduled on the UI thread.

UI elements can only be accessed on the thread they were created on (which is usually the UI thread).

### Parallel class
CPU-bound operatie.
impliciet van Task class.
Dit doe je alleen maar als je meer cores hebt dan taken.
```cs
for (int i = 0; index < 5; index++)
{
	Process(index);
}

Parallel.For(0,5, (index) => Process(index))
```

loopState.Break();
loopState.Stop();

### PLINQ
Parallel vorm van LINQ.
Wellicht verbeterd het de execution snelheid.

```cs
var result = from n in Enumerable.Range(1, 1000).AsParallel()
			 where n % 3 == 0
			 select n;
foreach (int i in result) 
{
	cwl($"{i}, {Thread.CurrentThread.ManagedThreadId}");
}
```
