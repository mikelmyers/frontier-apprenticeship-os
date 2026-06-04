# Lesson 002 — Coordinates and Vectors

## Objective

Understand coordinates as individual axis values and vectors as grouped values that can represent position, velocity, acceleration, force, or direction.

## 1. Plain-English Concept

A coordinate tells you where something is along one axis.

A vector is a group of coordinates.

In 3D space, we usually use three coordinates:

```text
x, y, z
```

A 3D vector looks like:

```text
[10, 5, 2]
```

That means:

```text
x = 10
y = 5
z = 2
```

## 2. Why This Matters for Trailblazer

Space infrastructure is not happening on a flat map. A depot, vehicle, drone, robotic arm, or cargo module exists in 3D space.

Vectors let us describe:

- where something is
- how it is moving
- what direction it is pointing
- what force is acting on it

The same basic structure appears again and again.

## 3. Notation Decoder

You may see:

```text
r = position vector
v = velocity vector
a = acceleration vector
F = force vector
```

The letters change, but the vector idea stays the same: multiple components grouped together.

Example:

```text
r_vehicle = [10, 5, 2]
```

Plain English:

> The vehicle's position is x = 10, y = 5, z = 2.

## 4. Small Numeric Example

```text
position = [10, 5, 2]
velocity = [1, 0, 0]
acceleration = [0, -0.1, 0]
```

Position tells us where the object is.

Velocity tells us how position is changing.

Acceleration tells us how velocity is changing.

Do not worry about calculating motion yet. Just learn the vocabulary.

## 5. Python Implementation

Create this file:

```text
exercises/000-foundation-bridge/002_coordinates_and_vectors.py
```

Type this manually:

```python
position = [10, 5, 2]
velocity = [1, 0, 0]
acceleration = [0, -0.1, 0]

print("Position:", position)
print("Velocity:", velocity)
print("Acceleration:", acceleration)

print("x position:", position[0])
print("y position:", position[1])
print("z position:", position[2])
```

## 6. Expected Output

```text
Position: [10, 5, 2]
Velocity: [1, 0, 0]
Acceleration: [0, -0.1, 0]
x position: 10
y position: 5
z position: 2
```

## 7. Concept Check

Python lists use index positions.

```text
position[0] = x
position[1] = y
position[2] = z
```

This is easy to forget at first. Python starts counting at 0.

## 8. Modification Exercise

Create a new vector:

```python
force = [0, 0, -9.8]
```

Print each component separately:

```text
x force
y force
z force
```

Then write one sentence explaining what the vector means.

## 9. Short Quiz

Create this file:

```text
quizzes/000-foundation-bridge/002_coordinates_and_vectors.md
```

Answer:

1. What is a coordinate?
2. What is a vector?
3. What does `position[0]` mean?
4. What does a velocity vector describe?
5. Why do spacecraft systems use vectors?

## 10. Completion Standard

You are done when:

- the Python file runs
- you can explain x, y, and z
- you can explain why vectors are used for position, velocity, and acceleration
