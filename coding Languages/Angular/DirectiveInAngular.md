# directive in angular

## Component Directives

Components have their own templates, styles, and can have inputs and outputs.

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

## Structural Directives

1. Structural directives are used to manipulate the structure of the DOM by adding, removing, or altering elements.

2. They typically use an asterisk (*) prefix in the template.
    Examples of structural directives include `*ngIf`, `*ngFor`, and `*ngSwitch`.

Example (using *ngFor):

```html
<ul>
  <li *ngFor="let item of items">{{ item }}</li>
</ul>
```

## Attribute Directives

1. Attribute directives are used to modify the appearance or behavior of elements.

2. hey are typically applied as HTML attributes.

    Examples for some built-in Angular attribute like `ngStyle` and `ngClass`, and you can create custom attribute directives as well.

Example (using ngStyle):

```html
<div [ngStyle]="{'color': 'blue', 'font-size': '16px'}">Styled Text</div>
```

## Custom Directives

1. You can create your own custom directives in Angular to encapsulate specific behavior or functionality.

2. Custom directives are typically used when you need to encapsulate reusable DOM manipulation logic.

    Example (custom directive to highlight an element on hover):

```typescript
import { Directive, ElementRef, HostListener, Input } from '@angular/core';

@Directive({
  selector: '[appHighlight]'
})
export class HighlightDirective {
  @Input() highlightColor: string = 'yellow';

  constructor(private el: ElementRef) {}

  @HostListener('mouseenter') onMouseEnter() {
    this.highlight(this.highlightColor || 'yellow');
  }

  @HostListener('mouseleave') onMouseLeave() {
    this.highlight(null);
  }

  private highlight(color: string | null) {
    this.el.nativeElement.style.backgroundColor = color;
  }
}
```

### HostListener vs HostBinding

@HostListener:

Purpose: @HostListener is used to listen to events on the host element (the element to which the directive is applied).

Usage: It is typically used in custom directives to define event listeners on the host element.

Example:

```typescript
import { Directive, HostListener } from '@angular/core';

@Directive({
  selector: '[appClickHighlight]'
})
export class ClickHighlightDirective {
  @HostListener('click') onClick() {
    // Code to execute when the host element is clicked
  }
}
```

In this example, the @HostListener decorator is used to listen for the click event on the host element and execute a function when the element is clicked.

@HostBinding:

Purpose: @HostBinding is used to bind a value to a property of the host element.

Usage: It is typically used to modify the host element's properties or attributes based on the state of the directive.

Example:

``` typescript

import { Directive, HostBinding } from '@angular/core';

@Directive({
  selector: '[appActiveHighlight]'
})
export class ActiveHighlightDirective {
  @HostBinding('class.active') isActive = false;

  toggleActive() {
    this.isActive = !this.isActive;
  }
}
``````

In summary, @HostListener is used for listening to events on the host element and responding to them, while @HostBinding is used for binding values to host element properties or attributes. These decorators are commonly used in custom directives to manipulate the behavior and appearance of host elements.

---
