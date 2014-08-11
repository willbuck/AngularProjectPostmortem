## Angular Services

- Make these fat (little / no logic in Controllers)
- Just use .factory, clearer than .service and not much difference
- Give these their own module for sharing

note:
	- .Service is new'd up
	- Useful if you need to do some setup immediately executing stuff, we haven't
	- Modules: useful for sharing individual services, up to you though
