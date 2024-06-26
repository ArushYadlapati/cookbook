# Complete TrajectoryBuilder Reference

### Ingredients

1. A fully tuned Road Runner 1.0 setup _**or**_ [MeepMeep for Road Runner 1.0](https://github.com/acmerobotics/MeepMeep)

### The Problem

The current [TrajectoryBuilder Reference](https://rr.brott.dev/docs/v1-0/builder-ref/) in 
the official Road Runner 1.0 docs only has a few TrajectoryBuilder methods, and does
not explain them very well in depth. This is a complete reference for more methods in
the TrajectoryBuilder class for Road Runner 1.0.

## TrajectoryBuilder Reference

### Path Primitives #

The begin pose is the origin (0,0) with a heading of $\frac{\pi}{6}$.

#### `lineToX(x: double)` & `.lineToXConstantHeading(x: double)`

🚨 WARNING: It is **HIGHLY RECOMMENDED** to use [`.strafeTo()`](https://github.com/ArushYadlapati/cookbook/blob/main/src/roadrunner_10/complete_trajectorybuilder_reference.md#strafetonew-vector2ddouble-x-double-y--strafetoconstantheadingnew-vector2dx-double-y-double) instead of any `lineTo()`'s! 🚨 

```java
// Robot moves to the specified x coordinate in the direction of the robot heading (straight line).
// Both `lineToX()` and `lineToXConstantHeading()` do the exact same thing and are effectively the same.
// 🚨 Will cause an error if your heading is perpendicular to direction your robot is traveling! 🚨

.lineToX(48)
.lineToXConstantHeading(48)
```

#### `lineToY(y: double)` & `.lineToYConstantHeading(y: double)`

🚨 WARNING: It is **HIGHLY RECOMMENDED** to use [`.strafeTo()`](https://github.com/ArushYadlapati/cookbook/blob/main/src/roadrunner_10/complete_trajectorybuilder_reference.md#strafetonew-vector2ddouble-x-double-y--strafetoconstantheadingnew-vector2dx-double-y-double) instead of any `lineTo()`'s! 🚨

```java
// Robot moves to the specified y coordinate in the direction of the robot heading (straight line).
// Both `lineToY()` and `lineToYConstantHeading()` do the exact same thing and are effectively the same.
// 🚨 Will cause an error if your heading is perpendicular to direction your robot is traveling! 🚨

.lineToY(36)
.lineToYConstantHeading(36)
```

#### `.strafeTo(new Vector2d(double: x, double: y))` & `.strafeToConstantHeading(new Vector2d(x: double, y: double))`

```java
// Robot moves to the specified coordinates while maintaining the heading.
// Both `strafeTo()` and `strafeToConstantHeading()` do the exact same thing and are effectively the same.
// So, if you start at a 90 degree angle, it will keep that angle the entire path.

.strafeTo(new Vector2d(48, 48))
.strafeToConstantHeading(new Vector2d(48, 48))

```

*Last Updated: 2024-07-02*