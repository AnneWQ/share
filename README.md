# share
angular basic
---------------------------------------
Module
Component
Template
Metadata
Data Binding
---------------------------------------
##Module
root module
Launch an application by bootstrapping its root module
Angular libraries
```typeScript

import { NgModule }      from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';
@NgModule({
  imports:      [ BrowserModule ],
  providers:    [ Logger ],
  declarations: [ AppComponent ],
  exports:      [ AppComponent ],
  bootstrap:    [ AppComponent ]
})
export class AppModule { }

```
---------------------------------------
---------------------------------------
---------------------------------------

##Component

+ HTML template + Component class
+ control patch of screen
+ Begins with @Component decorator function: metadata object

```typeScript

import { Component } from '@angular/core';

@Component({
  selector: 'my-app',
  template: `<h1>Hello {{name}}</h1>`
})
export class AppComponent { name = 'Angular'; }

```
---------------------------------------
##Template

+Angular's template syntax

+custom element

```typeScript
<h2>Hero List</h2>
<p><i>Pick a hero from the list</i></p>
<ul>
  <li *ngFor="let hero of heroes" (click)="selectHero(hero)">
    {{hero.name}}
  </li>
</ul>
<hero-detail *ngIf="selectedHero" [hero]="selectedHero"></hero-detail>
```

---------------------------------------
#Metadata

process a class
configuration object
---------------------------------------
#Data Binding
+{{}}
+[]
+()
+[()] child Component

---------------------------------------
#Directive
transforms the DOM according to the instructions given by directives

directive-with-a-template
structural: ngfor,ngIf
attribute:ngModel
---------------------------------------
#Service
fetch data from the server
validate user input
log directly to the console
---------------------------------------
#Dependency injection

---------------------------------------
