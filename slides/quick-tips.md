### Some quick tips

- Controller vs Ctrl
- use your own prefix for directives (NOT ng-, we use vw-)
- wrap scope values in object
- use $scope.$digest vs $scope.apply()


note:
- $scope.$apply runs $rootScope.digest and dirty checks the entire scope.
