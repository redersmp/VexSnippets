# Adding movement

#### Give any point velocity a normal

```
@v = @N;
```

Attach the above to pop network.

#### Move any point upwards

```
// point normal in y
@N = {0,1,0};

// set velocity to the new normal
@v = @N;
```

Attach the above to pop network.