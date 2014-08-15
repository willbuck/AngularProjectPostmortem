##  Gotchas: Security Roles & Permissions

-
```
 core.config ($provide) ->
     profile = angular.copy(window.myActiveProfile)
     $provide.constant('activeProfile', profile)
```

note:
- started out using interceptor to capture url to go to and then load log in module
- requirements didn't need that, and there was some so moved to static log on page
