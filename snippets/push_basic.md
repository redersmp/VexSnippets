# Pushing points

#### Push points along their normal

```
// create amount parameter
float amount = chf('Amount');

// update position
@P += @N * amount;
```

#### Push points along their normal, over time

```
@P += @N * @Frame;
```