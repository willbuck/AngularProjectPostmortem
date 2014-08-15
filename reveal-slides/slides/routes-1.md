```
.state 'case',
    abstract: true
    url: '/case'
    templateUrl: 'case.html'
.state 'case.tabs',
    views: {
        "tabs@case" : {templateUrl: 'tabs.html'}
        "customHeader@case" : { templateUrl: 'custom_header1.html'}
    }
.state 'case.tabs.profile',
    url: '/profile/:profileId'
    templateUrl: 'profile/main.html'
    resolve:
        patientProfile: ($stateParams, ProfileService) ->
            ProfileService.fetch $stateParams.profileId
```

```
<a ui-sref="case.tabs.profile({profileId:profile.id})">Profile</a>
```

```
$state.go("case.tabs.#{tab}", routeParams)
```

```
# TODO this kinda sucks how can we do better
if useRelative then  relativePathPrepend = '^'
if TreatmentActivityService.isActivityTreatmentPlan(treatmentActivity)
    $state.go(relativePathPrepend + '.plan', {
      encounterId: $stateParams.encounterId,
      workUnitId: $stateParams.workUnitId
    })
else if TreatmentActivityService.isActivityCaseNote(treatmentActivity)
    $state.go(relativePathPrepend + '.note', {
      encounterId: $stateParams.encounterId,
      workUnitId: $stateParams.workUnitId
    })
```
