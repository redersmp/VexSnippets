# Create a basic line
Create a simple polyline from a variable number of points.

```
// create point count parameter
int pointCount = chi("Point_Count");

// declare points array
int points[];

// resize array to point count size
resize(points, pointCount);

// loop through array
for(int i = 0; i < pointCount; i++) {
	// create new vector
	vector pos = set(0, i, 0);

	// create point at vector
	int point = addpoint(geoself(), pos);

	// add to array
	points[i] = point;
}

// add polyline primitive
addprim(geoself(), "polyline", points);
```