##  testing

- breaking code base into modules was the biggest challenge to testing
- unit test needs module under test to have comprehensive dependency definitions, no cheating!
- wrote custom matcher for deep comparison testing
- introducing restangular added new challenge for comparison
- wrote unit test for filters, directives, controllers, factories
- $httpBackend.flush() to ensure all async request are done
- rootScope.$apply() triggers $digest cycle to ensure all changes take effect

```
angular.equals(obj1, obj2)
```

note:
- restangular adds additional angular methods and properties to raw objects
- need to use Restangular.stripRestangular to get the raw object to do comparison in tests.
- testing watches want to use $apply
- can be code smell for immediate controller execution, consider resolve block
- want service calls to complete use flush
- 
