# Set geometry colour

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