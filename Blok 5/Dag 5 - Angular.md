### Agenda
- Formulieren met validatie
- Componenten maken en testen
### Forms
FormGroup
FormControl:
- In reactive forms each form element in the view is directly linked to the FormControl

### ReactiveForms Module
In reactive forms, the form's structure and logic is mostly handled in the component class, rather than the template. This gives you more control over the form behavior and allows you to handle more complex validation and interaction scenarios.

### App Routing Module .ts
Angular provides the `[Router](https://angular.io/api/router/Router)` service to help you define navigation paths among views. The router provides sophisticated in-browser navigational capabilities.

### Directives
A directive is a class that can add behavior to an element in your Angular templates. It's one of the key building blocks in Angular and enables you to create custom HTML-like elements or custom attributes for existing elements.

3 types of directives:
- Component Directive
- Attribute Directive
	- Change the appearance or behavior of an element, component, or another directive.
	```html
	<div> [ngStyle] ="{'color': 'red'}">This is red text. </div>
	```
- Structural Directive
	- Changed DOM layout
	```angular
	*ngFor
	*ngIf*
	```

### Prototypes
Soort extensions methods in C#

### Partial


### Componenten
`ng generate component components/lifecycle`
`ng g c components/lifecycle`
Deze angular cli commands maken een nieuwe map (of bestaande map) met daarin 3 components. Ook update het de module file met de juiste component.

- Lifecycle


- herbruikbaar UI-component


----------------------
## My own notes:

- **Property Binding** with `[]` is typically used when you want to bind a DOM property (like `src`) to a component property.
    
- **Interpolation** with `{{ }}` is used when you want to interpolate a value within text content or attribute values.

### Services
M any different use cases/purpuses.
Injectable tells angular it's usable in as Dependency Injection. Meaning other parts in the program can request a instance of the service.

Angular cli
`ng g s services/housing`
`ng generate service --path=app/services/housing`





