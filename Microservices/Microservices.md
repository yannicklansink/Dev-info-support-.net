Microservices are responsible for doing 1 thing well.
Organisatorisch op een lijn.

Voordelen:
- Easier to change and deploy (small and decoupled)
- Can be built using different technologies
- Resilient: 1 service can break, the other keeps running
- Scalable: You can scale out only the services you need to
- Built to be replaceable

### Docker
```bash
docker build -t yannicklansink/commandservice .

docker run -p 8080:80 -d yannicklansink/commandservice

docker push  yannicklansink/commandservice
```

### Kubernetes
Voor het beheer van containerized applicaties (bijv. een docker container) te automatiseren en te vergemakkelijken. 

commands:
```bash
# You need to be in the same folder as your files to apply these commands
# -f specifies a file path follows after
kubectl apply -f platforms-depl.yaml
kubectl delete deployment platforms-depl

kubectl get pods
kubectl get deployments

# will cause Kubernetes to gradually replace the existing Pods of the "platforms-# depl" Deployment with new ones.
# the recently built new pushed docker image will 
# cause Kubernetes to pull the new image and update the Pods 
# in Deployment one by one, ensuring that the application remains 
# available during the update process.
kubectl rollout restart deployment platforms-depl
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

### Ingress Nginx controller
