##  Gotchas: UI-Router Nested States

```
.state 'followUpNote.tabs.treatment',
  url: '/treatment/:encounterId/:workUnitId'
  templateUrl: '/angular/scripts/treatment/readable.html'
  controller: 'ReadableTreatmentTabController'
  resolve:
      patientProfile: ($stateParams, PatientProfileService) ->
          PatientProfileService.fetch $stateParams.encounterId
.state 'followUpNote.tabs.treatment.plan',
  views: {
      "content@followUpNote.tabs.treatment": {templateUrl: '/angular/scripts/treatment/_tpViewReadable.html'}
  }
.state 'followUpNote.tabs.treatment.note',
  views: {
      "content@followUpNote.tabs.treatment": {templateUrl: '/angular/scripts/followup/_noteDisplay.html'}
  }
```

```
$scope.goToProperActivityRoute = (treatmentActivity, useRelative) ->
    relativePathPrepend = ''
    if useRelative then  relativePathPrepend = '^' # TODO this kinda sucks how can we do better
    if TreatmentActivityService.isActivityTreatmentPlan(treatmentActivity)
        $state.go(relativePathPrepend + '.plan', {encounterId: $stateParams.encounterId, workUnitId: $stateParams.workUnitId})
    else if TreatmentActivityService.isActivityCaseNote(treatmentActivity)
        $state.go(relativePathPrepend + '.note', {encounterId: $stateParams.encounterId, workUnitId: $stateParams.workUnitId})
```

note:
Sibling nested views that you get to both from a 4th nesting and a 3rd, tough
