# Date Range Picker with inline for Angular and Bootstrap

Angular.js directive with inline by twinning [Angular DaterangePicker](https://github.com/fragaria/angular-daterangepicker).

Image(http://prntscr.com/j1xk5a)

## Installation

Please reference of [here](https://github.com/fragaria/angular-daterangepicker)

## Basic usage
Assuming that bower installation directory is `bower_components`. In case of other installation directory, please update paths accordingly.

```
<script src="bower_components/jquery/jquery.js"></script>
<script src="bower_components/angular/angular.js"></script>
<script src="bower_components/momentjs/moment.js"></script>
<script src="js/daterangepicker.min.js"></script>
<script src="js/angular-daterangepicker.min.js"></script>

<link rel="stylesheet" href="bower_components/bootstrap/dist/css/bootstrap.css"/>
<link rel="stylesheet" href="bower_components/bootstrap-daterangepicker/daterangepicker-bs3.css"/>
<link rel="stylesheet" href="css/style.css"/>
```
daterangepicker.min.js - twinned with bootstrap daterangepikcer
angular-daterangepicker.min.js - twinned with angular-daterangepicker
style.css  - custome css

Declare dependency:

```
App = angular.module('app', ['daterangepicker']);
```

Prepare model in your controller. The model **must** have `startDate` and `endDate` attributes:

```
exampleApp.controller('TestCtrl', function ($scope) {
	$scope.datePicker.date = {startDate: null, endDate: null};
}
```


Then in your HTML just add attribute `date-range-picker` to any input and bind it to model.

```
<div ng-controller="TestCtrl">
<input date-range-picker class="form-control date-picker" type="text" ng-model="datePicker.date" />
</div>
```

In case of using with inline, follow as

```
<div ng-controller="TestCtrl">
<div inline='true' date-range-picker class="form-control date-picker"ng-model="datePicker.date" />
</div>
```

See `example.html` for working demo.

## Advanced usage
 Other all options are same as [Angular DaterangePicker](https://github.com/fragaria/angular-daterangepicker)

Thanks you!