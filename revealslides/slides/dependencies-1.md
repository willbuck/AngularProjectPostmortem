
```
"dependencies": {
    "angular-mocks": "~1.2.16",
    "angular-scenario": "~1.2.16",
    "es5-shim": "~2.0.8",
    "angular-resource": "~1.2.16",
    "angular-cookies": "~1.2.16",
    "angular-sanitize": "~1.2.16",
    "angular-bootstrap": "~0.10.0",
    "jquery": "2.0.3",
    ...
}
```

development vs ci, everyone is at a different party


note:
    - this is a bower dependency list, node has a similar structure for server side dependencies
    - version equivalent essentially allows for auto updates (look at bower info angular-sanitize)
    - this would lead to occasional dependency issues with other packages.
    - delete all dependencies for both npm and bower, clean the cache, and then reinstall. to ensure everyone is running the same stuff
