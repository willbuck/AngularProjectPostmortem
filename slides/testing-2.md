`karma.conf.js`
```
    files: [
    		'web-app/vendors/**/*.js',
            'web-app/js/**/app.js',
            'web-app/js/**/*Module.js',// need to load all the modules first
    		'web-app/js/**/*.js',
    		'test/**/*.coffee'
    ],

    // enable / disable watching file and executing tests whenever any file changes
    autoWatch: true,

    // Continuous Integration mode
    // if true, it capture browsers, run tests and exit
    singleRun: false

```

note:
    Put your speaker notes here.
    You can see them pressing 's'.
