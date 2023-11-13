# Angular

![Angular Lifecycle](/lifecycle/img/angular-lifecycle.png "Angular Lifecycle")


## xxxInit
- All the 'xxxInit' hook will only be called **once**.

## ngOnChanges
- Respond when Angular **sets or resets** data-bound input properties (@Input()). 
- The method receives a SimpleChanges object of current and previous property values.
- Called before ngOnInit() (if the component has bound inputs) and whenever one or more data-bound input properties change.
- Note: If your component has no inputs or you use it without providing any inputs, the framework will not call ngOnChanges().
- Note: This happens frequently, so any operation you perform here impacts performance significantly.

## ngDoCheck
- Most of the time, it handled by Angular framework.

## ngAfterContentxxx
```html
<ExampleComponent>
    <!-- This is 'Content' -->
    <p>A paragraph</p>
    <!-- 'Content' end-->
</ExampleComponent>
```

This is the ExampleComponent Template
```html
<p>I am ExampleComponent</p>
<ng-content></ng-content>
```

Note: If there is no <ng-content>, the ```<p>Here is 'Content'</p>``` will not be shown.

## ngAfterViewxxx
This is the ExampleComponent Template
```html
<!-- This is 'View' -->
<p>I am ExampleComponent</p>
<ExampleChildComponent></ExampleChildComponent>
<!-- 'View' end-->
<ng-content></ng-content>
```