### modules
- how to organize
- directives, filters (and services?) are common
- naming, be consistent

```
  angular.module('profile.notes', ['ui.router', 'ui.bootstrap', 'profile.patient.api', 'profile.notes.api'])
      .controller('ProfileNotesController',
        function($scope, $stateParams, $location, $modal, ProfileNotesService, PatientProfileService) {
```

note:
    - started by breaking things up by type, controller, directive, filters, services
    - That's generally considered bad now
    - How "pure" do you want your modules?
    - Services can live in them, depends on your needs
