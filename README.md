opinionated-angular
===================

AngularJS, with a focus on maintainability and reusablity.


###ng-controller, ng-include VS custom directives

ng-controller should never be used.

Rather, create a custom directive.

- Building directives first is an easy yet impactful step toward reusability
and therefore maintainability. Widgets and web components are pieced together
all over your app, and a strong set of directives makes your life easy.
- Controller scope inheritance is often "convenient" for the first dev, and
"WTF" for the second. Directives provide an explicit intent and scope to work
with, with functionality happily encapsulated.

These reasons also apply to ng-include. A directive with a templateUrl is DRYer
the very next time that ng-include is needed.

###Factory, Service, Resource?

Where possible, a $resource should be used to represent any api endpoint.

Services tend to be convenient places for any data manipulation or logic that needs to happen between the resource and a controller.

