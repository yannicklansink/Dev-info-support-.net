Microservices are responsible for doing 1 thing well.
Organisatorisch op een lijn.

Voordelen:
- Easier to change and deploy (small and decoupled)
- Can be built using different technologies
- Resilient: 1 service can break, the other keeps running
- Scalable: You can scale out only the services you need to
- Built to be replaceable

### Kubernetes
Voor het beheer van containerized applicaties (bijv. een docker container) te automatiseren en te vergemakkelijken. 

commands:
```bash
kubectl apply -f platforms-depl.yaml
kubectl delete deployment platforms-depl

kubectl get pods
kubectl get deployments
```

### .NET CLI commands
```cli
dotnet add package AutoMapper.Extensions.Microsoft.DependencyInjection
dotnet add package Microsoft.EntityFrameworkCore
dotnet add package Microsoft.EntityFrameworkCore.Design
dotnet add package Microsoft.EntityFrameworkCore.InMemory
dotnet add package Microsoft.EntityFrameworkCore.Tools

dotnet remove package Microsoft.EntityFrameworkCore.InMemory   
```

