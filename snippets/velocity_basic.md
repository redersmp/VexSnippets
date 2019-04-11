# Adding movement

#### Initialise velocity from a surface normal

```
@v = @N;
```

#### Initialise velocity along the z-axis

```
@v = {0,0,1};
```

#### Move any point upwards

```
// point normal in y direction
@N = {0,1,0};

// set velocity to the new normal
@v = @N;
```

Attach the above to pop network to visualise.

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