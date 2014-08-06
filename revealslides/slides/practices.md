### A word on best practices

- Controller vs Ctrl
- use prefix for directives
- wrap scope values in object
- use $scope.$digest vs $scope.apply()


- tutorials not very helpful
- ng-book very helpful
- ng-conf very helpful


note:
    - typically everything is bundled in one file
    - started by breaking things up by type, controller, directive, filters, services
    - $scope.$apply runs $rootScope.digest and dirty checks the entire scope.
