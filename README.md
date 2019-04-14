# VEX Snippets

## Code snippets and examples of VEX inside Houdini

VEX is a small, efficient, general purpose language for writing shaders and custom nodes.

### VEX basics
When focus is on the code window, the keyboard shortcut `alt + e` opens the Houdini script editor.

When editing in the code window, press `ctrl + return` to commit the change and update Houdini.

Trigonometry functions such as `sin` and `cos` use radians, not degrees.

Exit a code snippet early using the `return` statement.

#### Reading parameters
The ch*() functions evaluate a parameter and return its value.
```
float scale = chi("Scale");
```

#### User functions
User functions must be declared before they are referenced and do not support recursion.
```
function int maximum(int a, b) {
	if (a > b) {
		return a;
	}
	return b;
}
```

#### Creating geometry

Create points, primitives, and vertices using `addpoint`, `addprim`, and `addvertex`. Alter geometry using `setattrib` and `setprimvertex`. Remove geometry using `removepoint` and `removeprim`.

#### Reading geometry attributes

Attributes that by convention are read / written by multiple node types.

| Variable | Description |
| --- | --- |
|@P|Point position.|
|@N|Normal direction.|
|@v|Velocity.|
|@pscale|Uniform scaling factor.|
|@Cd|Diffuse colour override.|

You don't need to specify the type of commonly used attributes.

#### Indexing variables
VEX can retrieve information while looping over points or primitives in geometry.

| Variable | Description |
| --- | --- |
|@ptnum|Point number of the current point.|
|@numpt|Total number of points in the current geometry.|
|@primnum|Primitive number of the current primitive.|
|@numprim|Total number of primitives in the current geometry.|

#### Global variables
VEX supports the following implicit variables.

| Variable | Description |
| --- | --- |
|@Time|Current time (in seconds).|
|@Frame|Current frame.|
