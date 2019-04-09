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

#### Blend between two objects
```
// get point position from second input
vector pos = point(1, "P", @ptnum);

// clamp time
float t = clamp(@Time, 0, 1);

// interpolate between current position and next, over time
vector between = lerp(@P, pos, t);

// set current point to new position
@P = between;
```
