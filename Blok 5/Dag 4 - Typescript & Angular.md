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

Component:
Herbruikbaar stuk code

Pipes in angular:
- date
- currency
met een verticaal streepje
date: {{date | date:'dd MMM yy' }}