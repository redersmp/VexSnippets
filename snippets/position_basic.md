# Locate nearby geometry

#### Match position on a surface

```
// match closest position from second input
vector pos = minpos(1, @P);

// move current position
@P = pos;
```

#### Match points on a surface

```
// match closest point from second input
int pt = nearpoint(1, @P);

// get position of point from second input
vector pos = point(1, "P", pt);

// move current position
@P = pos;
```

#### Join nearby points

```
// create radius parameter
float radius = chf("Search_Radius");

// match closest points within radius
int n[] = nearpoints(0, @P, radius);

// loop through matched points
foreach(int pt; n) {
	
	// if point matches current point skip it
	if(pt == @ptnum) continue;

	// create new polyline
	int line = addprim(0, "polyline");

	// add vertices to each end of line
	addvertex(0, line, pt);
	addvertex(0, line, @ptnum);
}
```