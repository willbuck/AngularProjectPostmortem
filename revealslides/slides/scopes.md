## Scopes

- glue between view and controller


note:
    - pass by val vs ref
    - other best practices? (don't inherit, too magical)
    - Batarang (whats the better one? figure out hwo to use it)


_.mixin({
        bindArray: (origArray, newArray) ->
            if newArray and origArray
                origArray.length = 0
                origArray.push(val) for val in newArray
    })
