# AngularJS Modules
1. An AngularJS module defines an application.
1. The module is a container for the different parts of an application.
1. The module is a container for the application controllers.
1. Controllers always belong to a module.

## Creating a Module
A module is created by using the AngularJS function `angular.module`
```js
<div ng-app="myApp">...</div>

<script>
   var app = angular.module("myApp", []); 
</script>
```

## Example
Add a controller to your application, and refer to the controller with the `ng-controller` directive:

```js
<div ng-app="myApp" ng-controller="myCtrl">
   {{msg}}
</div>

<script>
   var app = angular.module("myApp", []); 
   
   app.controller("myCtrl", function($scope) {
     $scope.msg = "Hello World";
   });
   
</script>
```

