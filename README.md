# ToDoList

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 11.0.7.
## Setting up
1. run script in terminal `ng new ToDoList` answer the questions of script
	> If the script could not complete within 5 minutes, 
	>	. Stop it using keyboard key `CTRL + C`
	>	. Change directory to `ToDoList` using command `CD ToDoList`, then run `npm install` and wait it to finish.
2. Change directory to newly created project using command `CD ToDoList` if you are not yet in it
3. Create a new component by running command `ng generate component ToDoItems`
4. Create file `/src/app/to-do-item.ts` with content:
	``` javascript
	export class ToDoItem{
	  id: number = 0;
	  name: string = '';
	  isComplete: boolean = false;
	}
	```
5. Configure `ToDoItems` component to use class `ToDoItem`.
6. update `/src/app/app.component.html` to use `<app-to-do-items></app-to-do-items>`
7. run application `ng serve --open`

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
