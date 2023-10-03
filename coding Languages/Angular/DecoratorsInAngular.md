# decorators in angular

## @Component

This decorator is used to define a component in Angular.

It provides metadata about the component, such as its selector, template or templateUrl, styles or styleUrls, and more.

    Example:

```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'app-my-component',
  templateUrl: './my-component.component.html',
  styleUrls: ['./my-component.component.css']
})
export class MyComponent { }
```

## @Injectable:

Used to define a service in Angular.

It tells Angular that the class can be injected as a dependency into other components or services.

    Example:

```typescript
import { Injectable } from '@angular/core';

@Injectable({
  providedIn: 'root'
})
export class MyService { }
```

## @NgModule

This decorator is used to define a module in Angular.

It provides metadata about the module, such as declarations (components, directives, and pipes), imports (other modules to import), exports (what can be used by other modules), and providers (services to be registered at the module level).

Example:

```typescript

import { NgModule } from '@angular/core';

@NgModule({
  declarations: [MyComponent],
  imports: [CommonModule],
  exports: [MyComponent],
  providers: [MyService]
})
export class MyModule { }
```

## @Input and @Output

These decorators are used to define input and output properties for components.

@Input allows data to be passed into a component from its parent.

@Output allows events to be emitted from a component to its parent.

Example:

```typescript

import { Component, Input, Output, EventEmitter } from '@angular/core';

@Component({
  selector: 'app-my-component',
  template: `
    <div>{{ inputData }}</div>
    <button (click)="emitEvent()">Emit Event</button>
  `
})
export class MyComponent {
  @Input() inputData: string;
  @Output() customEvent = new EventEmitter<void>();

  emitEvent() {
    this.customEvent.emit();
  }
}
```
