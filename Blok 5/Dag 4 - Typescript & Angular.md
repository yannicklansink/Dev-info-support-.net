### Agenda
- Introductie: waarom Angular?
- Databinding basics: tekst, attributen, loops, if
- Data formatteren met pipes
- Custom pipe unittesten

Angular is een framework voor applicatieontwerp en een ontwikkelingsplatform voor het maken van efficiënte en geavanceerde apps met één pagina.

### Waarom angular
- Google
- SPA
- Open source
- Typescript

SPA - Single Page Application
- Alles wordt direct geladen
- Vooral gebruikt met veel interactie met de gebruiker

SSR - Server-side Rendering
- Rendered SEO eerst
- Om SPA te optimaliseren
- Next.js Nuxt.js Angular Universal/Analog ASP.NET CORE

MPA - Multi Page Application
- Server genereerd alle HTML

SSG - Static Site Generator
- bol.com
- Als je data hebt wat weinig veranderd?

### @angular/cli
- ng new <projectnaam>
- ng build - maak je project klaar voor deployment
- ng test - run unittest
- ng test --code-coverage - run unittest met coverage
- ng serve - lokaal web server opstarten met jouw gecompileerde code 

### Component:
Herbruikbaar stuk code.
Componenten zijn de bouwstenen van een Angular-applicatie. Een component bevat een TypeScript-class met een @Component() decorator.

### Pipes in angular:
- date
- currency
met een verticaal streepje
date: {{date | date:'dd MMM yy' }}

### Files that make up a component:
1. `app.module.ts`: Specifies the files that the application uses. This file acts as a central hub for the other files in your application.
2. `app.component.ts`: Also known as the class, contains the logic for the application's main page.
3. `app.component.html`: Contains the HTML for `AppComponent`. The contents of this file are also known as the template. The template determines the view or what you see in the browser.
4. `app.component.css`: Contains the styles for `AppComponent`. You use this file when you want to define styles that only apply to a specific component, as opposed to your application overall.

Jasmine is the standard test framework in angular
