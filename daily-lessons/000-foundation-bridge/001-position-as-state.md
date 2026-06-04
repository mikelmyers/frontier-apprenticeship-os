# Lesson 001 — Position as State

## Objective

Understand that position is a piece of system state: a stored value that tells us where an object is.

By the end of this lesson, you should be able to explain and write Python code for a depot position and a vehicle position.

## 1. Plain-English Concept

Position means where something is.

In aerospace, robotics, and simulation, position is not just a word. It is data.

A depot has a position. A vehicle has a position. A drone has a position. A sensor has a position. Before you can calculate distance, approach direction, velocity, or collision risk, you need a way to represent where each object is.

## 2. Why This Matters for Trailblazer

A Pin Depot cannot monitor an incoming vehicle unless both objects have known positions.

The most basic navigation question is:

> Where is the vehicle?

Only after that can we ask:

> How far away is it?
> Is it approaching?
> Is it approaching safely?
> Should the depot allow docking or trigger an abort?

## 3. Notation Decoder

You may eventually see position written like this:

```text
r
```

or:

```text
r_depot
r_vehicle
```

In many physics and aerospace contexts, `r` means position.

The subscript tells us which object's position we mean.

```text
r_depot = depot position
r_vehicle = vehicle position
```

For now, do not worry about fancy notation. Just remember:

```text
r usually means position.
```

## 4. Small Numeric Example

In one dimension:

```text
position = 10
```

This means the object is 10 units from the origin.

In three dimensions:

```text
position = [10, 5, 2]
```

This means:

```text
x = 10
y = 5
z = 2
```

So the object is 10 units along x, 5 units along y, and 2 units along z.

## 5. Python Implementation

Create this file:

```text
exercises/000-foundation-bridge/001_position_as_state.py
```

Type this manually:

```python
depot_position = [0, 0, 0]
vehicle_position = [10, 5, 2]

print("Depot position:", depot_position)
print("Vehicle position:", vehicle_position)

# The vehicle moves.
vehicle_position[0] = 12
vehicle_position[1] = 7
vehicle_position[2] = 3

print("Updated vehicle position:", vehicle_position)
```

## 6. Expected Output

```text
Depot position: [0, 0, 0]
Vehicle position: [10, 5, 2]
Updated vehicle position: [12, 7, 3]
```

## 7. Concept Check

The vehicle moved from:

```text
[10, 5, 2]
```

to:

```text
[12, 7, 3]
```

That means it moved:

- +2 in x
- +2 in y
- +1 in z

## 8. Modification Exercise

Change the starting vehicle position to:

```text
[50, -10, 8]
```

Then update it to:

```text
[45, -8, 8]
```

Answer:

1. Did x increase or decrease?
2. Did y increase or decrease?
3. Did z change?

## 9. Short Quiz

Create this file:

```text
quizzes/000-foundation-bridge/001_position_as_state.md
```

Answer:

1. What does position mean?
2. Why do we store position as data?
3. What does `[10, 5, 2]` represent?
4. What does `r_vehicle` mean in plain English?
5. Why does a depot need to know a vehicle's position?

## 10. Completion Standard

You are done when:

- the Python file runs
- you can explain what each list number means
- you can explain why position is the first requirement for navigation
