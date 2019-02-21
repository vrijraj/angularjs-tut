## AngularJS Directives

AngularJS directives are extended HTML attributes with the prefix ng-.
1. The `ng-app` directive initializes an AngularJS application.
1. The `ng-init` directive initializes application data.
1. The `ng-model` directive binds the value of HTML controls (input, select, textarea) to application data.

```html
  <div ng-app="" ng-init="firstName='John'">
    <p>Name: <input type="text" ng-model="firstName"></p>
    <p>You wrote: {{ firstName }}</p>
  </div>
```

Example 2

```html
  <div ng-app="" ng-init="quantity=1;price=5">
    Quantity: <input type="number" ng-model="quantity">
    Costs:    <input type="number" ng-model="price">
    Total in dollar: {{ quantity * price }}
  </div>
```
