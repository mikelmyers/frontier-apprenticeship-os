# Lesson 004 — Distance and Magnitude

## Objective

Understand that vector magnitude means length, and that the magnitude of relative position is the straight-line distance between two objects.

This lesson explains notation like:

```text
||r_rel||
```

## 1. Plain-English Concept

Relative position tells us how far apart two objects are along each axis.

Example:

```text
[80, 30, 5]
```

This says the vehicle is offset from the depot by:

- 80 in x
- 30 in y
- 5 in z

But that is not the same as straight-line distance.

Distance asks:

> How far apart are the two objects in a direct line?

## 2. Why This Matters for Trailblazer

A depot needs range information for:

- approach monitoring
- docking thresholds
- abort zones
- safe separation
- collision avoidance
- handoff between control modes

A vehicle may be offset in x, y, and z, but the depot needs one clean number for range.

## 3. Notation Decoder

You may see:

```text
||r_rel||
```

The double bars mean magnitude or length.

So:

```text
||r_rel||
```

means:

> the length of the relative position vector

In plain English:

> the distance between the depot and the vehicle

## 4. Small Numeric Example

If:

```text
r_rel = [3, 4, 0]
```

then the distance is:

```text
sqrt(3^2 + 4^2 + 0^2)
```

which becomes:

```text
sqrt(9 + 16 + 0)
```

which becomes:

```text
sqrt(25) = 5
```

So:

```text
||r_rel|| = 5
```

This is just the 3D version of the Pythagorean theorem.

## 5. Python Implementation

Create this file:

```text
exercises/000-foundation-bridge/004_distance_and_magnitude.py
```

Type this manually:

```python
import math

relative_position = [80, 30, 5]

x = relative_position[0]
y = relative_position[1]
z = relative_position[2]

distance = math.sqrt(x**2 + y**2 + z**2)

print("Relative position:", relative_position)
print("Distance:", distance)
```

## 6. Expected Output

The distance should be approximately:

```text
85.58621384311844
```

Rounded:

```text
85.59
```

## 7. Concept Check

This Python line:

```python
distance = math.sqrt(x**2 + y**2 + z**2)
```

is the code version of:

```text
||r_rel|| = sqrt(x^2 + y^2 + z^2)
```

So when you see:

```text
||r_rel||
```

read it as:

> distance between the two objects

## 8. Modification Exercise

Change the relative position to:

```python
relative_position = [3, 4, 0]
```

Before running the code, predict the distance.

Then run it.

Expected result:

```text
5.0
```

Then try:

```python
relative_position = [1, 2, 2]
```

Predict the distance manually.

## 9. Short Quiz

Create this file:

```text
quizzes/000-foundation-bridge/004_distance_and_magnitude.md
```

Answer:

1. What do the double bars `|| ||` mean?
2. What does `||r_rel||` mean in plain English?
3. Why is `[80, 30, 5]` not itself the distance?
4. What is the magnitude of `[3, 4, 0]`?
5. Why does a depot need range/distance information?

## 10. Completion Standard

You are done when:

- the Python file runs
- you can calculate a simple vector magnitude by hand
- you can explain why `||r_rel||` means distance
