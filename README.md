# Component architecture
In this repository you will find information what is component architecture on frontend. We hope that this will allow you to create code less prone to bugs, scalable and easier to maintain.

Component architecture consists of multiple patterns. Below you will find all patterns that are common for all current UI libraries and frameworks.

## Patterns
### Container/Presentational
#### Container Components
![smart component](images/smart-component.png)
characteristics:
* Have external dependencies
* Have side effects
* May have local state

Testability:
* Test with mocks or stubs

Tips:
* If you want to test container components do functional testing

Other names:
* Smart Components
* Smart Stateful Components
* Smart Stateless Components

#### Presentational Components
![dumb component](images/dumb-component.png)
characteristics:
* Have no external dependencies
* Have no side effects
* May have local state

Testability:
* Test with shallow rendering (not recommended)
* Test with snapshot testing
* Test with visual regression testing
* Test accessibility

Other names:
* Dumb Components
* Dumb Stateful Components
* Dumb Stateless Components

##### Screen Components
They are directly matched with routing and are responsible for composing other components to display a screen.

Those components should take data only from the URL and pass them further.

If this component takes and passes URL data it becomes a Smart Component. If not - dumb.

Those components should be as simple as possible.

Those types of components can be also called "Views Components".

### Compound Components
* set of components that are used together, are dependent on each other and cannot be used separately
* use only when creating component library
### Higher Order Components
* use only when developing library
* do not use HoCs that set states in application code

## Other solutions
### Server Components
* React solution for server side rendering
### Reusable Views and Modules
* Dependency Injection to reuse whole views or modules that look and behave the same but use different API

## Testing components
* Mocking with Mock Service Worker
* Page Object Pattern
* Component Object Pattern
* Visual Regression Testing
* Accessibility Testing
* Snapshot Testing
### Unit testing (Jest)
### Storybook
### E2E/Component testing libraries Cypress/Playwright
