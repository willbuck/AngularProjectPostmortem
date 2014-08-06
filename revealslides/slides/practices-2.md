### modules
- how to organize
- services, directives and filters are common
- naming, be consistent

```
  angular.module('profile.notes', ['ui.router', 'ui.bootstrap', 'profile.patient.api', 'profile.notes.api'])
      .controller('ProfileNotesController',
        function($scope, $stateParams, $location, $modal, ProfileNotesService, PatientProfileService) {
```

note:
    - started by breaking things up by type, controller, directive, filters, services
