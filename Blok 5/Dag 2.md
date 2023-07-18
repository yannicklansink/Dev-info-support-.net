Zodra je met lambdas werkt met locale variabelen moet je uitkijken wat je doet. Variabelen gaan dan naar de heap.

### Threadpool
- Teveel threads verminderen de performance
- Beste om 1 thread per core
	-  Oplossing => threadpool
- Creeer niet je eigen thread, maar stuur het naar de threadpool
	- ThreadPool.QueueUserWorkItem(o => );