## Angular Services

- Services everywhere with $resource
- $broadcast, $emit, $on, $watch
- Understanding promises with $http
- Moving to Restful services
- Custom endpoints
- Roll our own
- restangular (TODO Investigate)
	- nested requests
	- deal with objects or promises at same time
	- custom methods
	- element transformers
	- extend models
	- request and response and error interceptors

note:
	- we started by looking at the mock ups and just writing a lot of services to get the exact data we needed for the view
	- $resource, at the time, did not support promises. so we relied on $broadcast to notify changes to the data
	- promises are great and removed all the $broadcast and $on calls we were doing
	- we had way to many service calls and realized we need to clean up these calls to be more restful
	- $http has its limitations
	- doubleClick at ng-conf showed a way of wrapping $http to allow for custom endpoints and had a better way of testing service calls
	- way too much boiler plate code. started using restangular
	- NG-BOOK has Restangular in it, check there for more
