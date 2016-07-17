#ng-book Notes
=============

##The Basics of AngularJS

- Every computer has a unique address that tell the network how to reach it.

- IP: Internet Protocol

- In a shared network (like at Starbucks), your comp shares the same IP address as the other computers.  Your comp can be reached by its internal IP address.

- See the DNS server response by typing in the terminal: `dig google.com`

- MVC: Model-View-Controller

##Data Binding and Your First AngularJS Web Application

- The only elements that will be affected by Angular at the DOM elements that we declare inside of the one with the `ng-app` attribute.

- The MVC (Model-View-Controller) makes a clear division between objects in our web app so that the view doesn't need to know how to save an object - it just needs to know how to display it.  The model doesn't need to interact with the view (like jQuery), it just needs to contain the data and methods to manipulate the view.  The controller is where we'll place the logic to bind the two together.

- Dirty Value: a value that has changed since last time an event loop has run.

- $ is a symbol representing an Angular object.

- $scope is an object in the model object.  It is a JS object whose properties are all available to the view and with which the controller can interact.

`angular.module('myApp', []);
`
`angular.module('myApp').controller('MyController', function($scope, $timeout){
});`

- In the code above, we told Angular that we wanted to create a module named myApp by using `angular.module('myApp', [])`. The function `angular.module()` returns a module.

On the next line, we call the `.controller()` function on that module.

The `.controller()` function defines a new controller. It takes two arguments:

- The first argument MyController is a string that defines the name of the controller

- The second argument is a definition function that defines how the controller will work.

- The MyController definition function takes two parameters: the $scope of the DROM element and the $timeout.  This is called dependency injection.


##Modules

- The Angular module API allows us to declare a module using the `angular.module()` API method. When declaring a module, we need to pass two parameters to the method. The first is the name of the module we are creating. The second is the list of dependencies, otherwise known as injectables.

`angular.module('myApp', []);`

This method is called the *setter* method for the Angular module; it’s how we define
our module.

- We can always reference our module by using the same method with only one parameter. For
instance, we can reference the myApp module like so:

`// this method fetches the app
2 angular.module('myApp')`

This method is known as the *getter* method, whereby we can get the Angular module
for later reference.
