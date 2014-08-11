### Some quick tips 

- Controller vs Ctrl
- use prefix for directives
- wrap scope values in object
- use $scope.$digest vs $scope.apply()


note:
    - typically everything is bundled in one file
    - started by breaking things up by type, controller, directive, filters, services
    - $scope.$apply runs $rootScope.digest and dirty checks the entire scope.
