# Create a basic wave

Create a simple wave effect.

```
// create scale parameter
float scale = chf('Scale');

// calculate length from origin
float dst = length(@P);

// multiply distance by scale
dst *= scale;

// update y position of point
@P.y = sin(dst);
```