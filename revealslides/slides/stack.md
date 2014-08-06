## The Stack
- Grails + Angular
- Grunt
- Coffeescript
- Jasmine & Karma
- Bower
- SASS (& Compass)

note:
	- Grunt config files are a bit unruly, Gulp did look nice, but didn't work for us
	- Coffeescript, was quick to pick up, first you are looking at the js output, now not so much. setting up callback got me a few times
	- Jasmine, forces you to set up your dependencies correctly for testing.
	- added custom matchers for santizing restangular data for equality checks
	- Bower and Node installs caused us pains due to package dependencies. more on that later
	- SASS, a great way to modularizing your css.
	- We setup a shame sass file for developers to use which our resident stylist would then clean up.
	- Compass is a SASS framework of niceties, really helpful to have but requires ruby
