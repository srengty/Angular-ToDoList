# ToDoList

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 11.0.7.
## Setting up
1. run script in terminal `ng new ToDoList` answer the questions of script
	> If the script could not complete within 5 minutes, 
	>
	>	* Stop it using keyboard key `CTRL + C`
	>	* Change directory to `ToDoList` using command `CD ToDoList`, then run `npm install` and wait it to finish.
2. Change directory to newly created project using command `CD ToDoList` if you are not yet in it
3. Create a new component by running command `ng generate component ToDoItems`
4. Create file `/src/app/to-do-item.ts` with content:
	``` javascript
	export class ToDoItem {
	  id: number = 0;
	  name: string = '';
	  isComplete: boolean = false;
	}
	```
5. Configure `/src/to-do-items/to-do-items.component.ts` component to use class `ToDoItem`.
	``` javascript
	import { Component, OnInit } from '@angular/core';
	import {ToDoItem} from '../to-do-item';
	@Component({
	  selector: 'app-to-do-items',
	  templateUrl: './to-do-items.component.html',
	  styleUrls: ['./to-do-items.component.css']
	})
	export class ToDoItemsComponent implements OnInit {
	  toDoItem: ToDoItem = {
		id: 1,
		name: "Two books",
		isComplete: false
	  }
	  constructor() { }

	  ngOnInit(): void {
	  }

	}
	```
6. Update `/src/app/to-do-items/to-do-items.component.html` to display `toDoItem` attribute:
	``` html
	<p>to-do-items works!</p>
	<p>id: {{ toDoItem.id }}<br/>
	  name: {{ toDoItem.name }}<br/>
	  Completed: {{ toDoItem.isComplete }}
	</p>
	```
7. update `/src/app/app.component.html` to use `<app-to-do-items></app-to-do-items>`
	``` html
	<app-to-do-items></app-to-do-items>
	```
8. run application `ng serve --open`

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
