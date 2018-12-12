# AngularJS Expressions
AngularJS expressions can be written inside double braces: `{{ expression }}`.

AngularJS expressions can also be written inside a directive:  `ng-bind="expression"`.

AngularJS will resolve the expression, and return the result exactly where the expression is written.

AngularJS expressions are much like JavaScript expressions: They can contain literals, operators, and variables.

Example `{{ 5 + 5 }}` or `{{ firstName + " " + lastName }}`

* If you remove the ng-app directive, HTML will display the expression as it is, without solving it

## AngularJS Numbers
AngularJS numbers are like JavaScript numbers:
`{{ 5+5 }}`
Example:

```js
<div ng-app="" ng-init="a=1;b=5">
  <p>Sum: {{ a + b }}</p>
</div>
```
* Same example using `ng-bind`:
```js
<div ng-app="" ng-init="a=1;b=5">
  <p>Sum: <span ng-bind="a + b"></span></p>
</div>
```

## AngularJS Strings
```js
<div ng-app="" ng-init="firstName='Vrijraj';lastName='Singh'">
  <p>The name is {{ firstName + " " + lastName }}</p>
</div>
```
* Same example using `ng-bind`:
```js
<div ng-app="" ng-init="firstName='Vrijraj';lastName='Singh'">
  <p>The name is <span ng-bind="firstName + ' ' + lastName"></span></p>
</div>
```

## AngularJS Objects
```js
<div ng-app="" ng-init="person={firstName:'Vrijraj',lastName:'Singh'}">
  <p>The name is {{ person.lastName }}</p>
</div>
```

* Same example using `ng-bind`:
```js
<div ng-app="" ng-init="person={firstName:'Vrijraj',lastName:'Singh'}">
  <p>The name is <span ng-bind="person.lastName"></span></p>
</div>
```

## AngularJS Arrays
```js
<div ng-app="" ng-init="data=[1,15,19,2,40]">
  <p>The third result is {{ data[2] }}</p>
</div>
```

* Same example using `ng-bind`:
```js
<div ng-app="" ng-init="data=[1,15,19,2,40]">
  <p>The third result is <span ng-bind="data[2]"></span></p>
</div>
```
