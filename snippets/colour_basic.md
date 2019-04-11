# Set geometry colour

Unlike most variables @Cd initialises to 1 rather than 0. In a colour context this displays white by default rather than black.

#### Assign colour values to points and primitives

@Cd, @P and @N are all vector types, so it is easy to assign them to each other.
```
@Cd = @N;
```

```
@Cd = @P;
```

#### Create a colour ramp over geometry
```
@Cd = float(@ptnum) / @numpt;
```

#### Set points to random colour and scale

```
// create random vector values
vector rnd = rand(@ptnum);

// create scale property from vector
float scale = rnd.x;

// resize scale to smaller range
float ftScale = fit(scale, 0, 1, 0, 0.1);

// set colour
@Cd = rnd;

// set point scale
@pscale = ftScale;
```