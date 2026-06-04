# Lesson 005 — Relative Velocity

## Objective

Understand relative velocity: how fast one object is moving compared to another object.

This lesson introduces:

```text
v_rel = v_vehicle - v_depot
```

## 1. Plain-English Concept

Velocity means how position changes over time.

Relative velocity means:

> How fast is object B moving compared to object A?

If the depot is still and the vehicle is moving toward it, relative velocity tells us how quickly the situation is changing.

## 2. Why This Matters for Trailblazer

Position tells us where the vehicle is.

Distance tells us how far away it is.

Velocity tells us how fast it is moving.

Relative velocity tells us how fast it is moving compared to the depot.

A depot needs this to decide whether an approach is safe.

A vehicle that is close and slow may be safe.

A vehicle that is close and fast may require an abort.

## 3. Notation Decoder

You may see:

```text
v_depot
```

Plain English:

> the depot's velocity

You may see:

```text
v_vehicle
```

Plain English:

> the vehicle's velocity

You may see:

```text
v_rel
```

Plain English:

> the vehicle's velocity relative to the depot

The equation:

```text
v_rel = v_vehicle - v_depot
```

means:

> relative velocity equals vehicle velocity minus depot velocity

## 4. Small Numeric Example

Depot velocity:

```text
[0, 0, 0]
```

Vehicle velocity:

```text
[-2, -1, 0]
```

Relative velocity:

```text
[-2, -1, 0]
```

Plain English:

> Compared to the depot, the vehicle is moving negative 2 units per time step in x, negative 1 unit per time step in y, and 0 in z.

## 5. Python Implementation

Create this file:

```text
exercises/000-foundation-bridge/005_relative_velocity.py
```

Type this manually:

```python
depot_velocity = [0, 0, 0]
vehicle_velocity = [-2, -1, 0]

relative_velocity = [
    vehicle_velocity[0] - depot_velocity[0],
    vehicle_velocity[1] - depot_velocity[1],
    vehicle_velocity[2] - depot_velocity[2],
]

print("Depot velocity:", depot_velocity)
print("Vehicle velocity:", vehicle_velocity)
print("Relative velocity:", relative_velocity)
```

## 6. Expected Output

```text
Depot velocity: [0, 0, 0]
Vehicle velocity: [-2, -1, 0]
Relative velocity: [-2, -1, 0]
```

## 7. Concept Check

Velocity is movement per time step.

If the vehicle position changes from:

```text
[100, 40, 5]
```

to:

```text
[98, 39, 5]
```

then it moved:

```text
[-2, -1, 0]
```

That movement per time step is velocity.

## 8. Modification Exercise

Change the values to:

```python
depot_velocity = [1, 0, 0]
vehicle_velocity = [4, 2, 0]
```

Calculate relative velocity manually first.

Then run the code.

Expected result:

```text
[3, 2, 0]
```

## 9. Short Quiz

Create this file:

```text
quizzes/000-foundation-bridge/005_relative_velocity.md
```

Answer:

1. What does velocity mean?
2. What does relative velocity mean?
3. What does `v_rel` mean in plain English?
4. Why do we subtract depot velocity from vehicle velocity?
5. Why is relative velocity important for docking safety?

## 10. Completion Standard

You are done when:

- the Python file runs
- you can calculate relative velocity by hand
- you can explain why a depot cares about relative velocity
