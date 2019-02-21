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


## Repeating HTML Elements
`ng-repeat` directive repeats an HTML element:

```html
  <div ng-app="" ng-init="names=['Jani','Hege','Kai']">
    <ul>
      <li ng-repeat="x in names">
        {{ x }}
      </li>
    </ul>
  </div>
```

Example 2

```html
  <div ng-app="" ng-init="names=[
    {name:'Jani',country:'Norway'},
    {name:'Hege',country:'Sweden'},
    {name:'Kai',country:'Denmark'}]">

    <ul>
      <li ng-repeat="x in names">
        {{ x.name + ', ' + x.country }}
      </li>
    </ul>
  </div>
```

## Two-way Binding
Data binding in AngularJS is the synchronization between the model and the view.

When data in the model changes, the view reflects the change, and when data in the view changes, the model is updated as well. This happens immediately and automatically, which makes sure that the model and the view is updated at all times.

```html
    <div ng-app="myApp" ng-controller="myCtrl">
      Name: <input ng-model="firstname">
      <h1>{{firstname}}</h1>
    </div>

    <script>
    var app = angular.module('myApp', []);
    app.controller('myCtrl', function($scope) {
      $scope.firstname = "John";
      $scope.lastname = "Doe";
    });
    </script>
```

## AngularJS Controller
Applications in AngularJS are controlled by controllers. Read about controllers in the AngularJS Controllers chapter.

Because of the immediate synchronization of the model and the view, the controller can be completely separated from the view, and simply concentrate on the model data. Thanks to the data binding in AngularJS, the view will reflect any changes made in the controller.

```html
  <div ng-app="myApp" ng-controller="myCtrl">
    <h1 ng-click="changeName()">{{firstname}}</h1>
  </div>

  <script>
    var app = angular.module('myApp', []);
    app.controller('myCtrl', function($scope) {
      $scope.firstname = "John";
      $scope.changeName = function() {
        $scope.firstname = "Nelly";
      }
    });
  </script>
```
