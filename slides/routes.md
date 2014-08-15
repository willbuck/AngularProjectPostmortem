## Routes

- Started with ngRoute, quickly moved to ui.router
- ngRoute is based on routes in your application
- ui.router is based on what state your application is in
- ui.router allows for nested states and views
- ui.sref directive that binds anchor tags to states

note:
- had a tabing ui that we tried to setup using $route, but needed to load the universe for it to work.
- tried to put logic in services to controll when fetches happened. ugly
- $route only allows you to assign controllers and template to a url, not very flexible
- $state, allows for nested views, resolves, and named routes
