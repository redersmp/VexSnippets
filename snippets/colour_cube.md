# Colour cube faces

Set primitive colour based on normal direction.

```
if (abs(@N.x) >= 1) {
    // red
    @Cd = {1,0,0};
}
if (abs(@N.y) >= 1) {
    // green
    @Cd = {0,1,0};
}
if (abs(@N.z) >= 1) {
    // blue
    @Cd = {0,0,1};
}
```