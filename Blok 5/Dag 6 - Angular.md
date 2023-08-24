- Dependency injection met services
- Backendcommunicatie
- Reactive programming

### Dependency Injection
- Inversion of control
- low coupling

provideIn: 'root':
- beter voor optimalisatie
- beter voor grote projecten met tientallen services

### Services
- The _injector_ is the main mechanism. Angular creates an application-wide injector for you during the bootstrap process, and additional injectors as needed. You don't have to create injectors.
    
- An injector creates dependencies and maintains a _container_ of dependency instances that it reuses, if possible.
    
- A _provider_ is an object that tells an injector how to obtain or create a dependency

3 ways to provide services to compenents:
- Injectable
``` ts
@Injectable({
 providedIn: 'root',
})
```
- NgModule
- Component
``` ts
@Component({
  selector:    'app-hero-list',
  templateUrl: './hero-list.component.html',
  providers:  [ HeroService ]
})
```

### Testing
mock aanmaken manieren:
- SpyOn() -> functie maken
- `let navigateserviceMock = jasmine.createSpyOn('navigateServiceMock', ['next'])  ->`
- ng-mocks (download npm)

### Backendcommunicatie
npm: json-server
- Get a full fake rest api
- npm install --global json-server