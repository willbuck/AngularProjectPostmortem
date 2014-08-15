## Scopes

Beware of bind by value vs bind by reference

```
$scope.myBoolean = SomeService.thatBoolean
// Asking for trouble
SomeService.thatBoolean = false
// Will save you headaches
SomeService.thatBoolean = {value: false}
```

And for arrays...

```
_.mixin({
  bindArray: (origArray, newArray) ->
    if newArray and origArray
      origArray.length = 0
      origArray.push(val) for val in newArray
})
```

note:
- pass by val vs ref
- other best practices? (don't inherit, too magical)
- ng-inspector > Batarang
