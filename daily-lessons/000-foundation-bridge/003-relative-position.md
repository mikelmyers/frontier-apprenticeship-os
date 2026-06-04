# Lesson 003 — Relative Position

## Objective

Understand relative position: where one object is compared to another object.

This lesson introduces the first important aerospace notation pattern:

```text
r_rel = r_vehicle - r_depot
```

## 1. Plain-English Concept

Relative position means:

> Where is object B compared to object A?

If a depot is at one location and a vehicle is at another location, relative position tells us where the vehicle is from the depot's point of view.

## 2. Why This Matters for Trailblazer

Docking, rendezvous, inspection, avoidance, and depot operations all depend on relative position.

The depot does not only care where the vehicle is in the solar system. It cares where the vehicle is compared to the depot.

This is the start of approach monitoring.

## 3. Notation Decoder

You may see:

```text
r_depot
```

Plain English:

> the depot's position

You may see:

```text
r_vehicle
```

Plain English:

> the vehicle's position

You may see:

```text
r_rel
```

Plain English:

> the vehicle's position relative to the depot

The equation:

```text
r_rel = r_vehicle - r_depot
```

means:

> relative position equals vehicle position minus depot position

## 4. Small Numeric Example

Depot position:

```text
[20, 10, 0]
```

Vehicle position:

```text
[100, 40, 5]
```

Subtract component by component:

```text
x: 100 - 20 = 80
y: 40 - 10 = 30
z: 5 - 0 = 5
```

Relative position:

```text
[80, 30, 5]
```

Plain English:

> From the depot's perspective, the vehicle is 80 units away in x, 30 units away in y, and 5 units away in z.

## 5. Python Implementation

Create this file:

```text
exercises/000-foundation-bridge/003_relative_position.py
```

Type this manually:

```python
depot_position = [20, 10, 0]
vehicle_position = [100, 40, 5]

relative_position = [
    vehicle_position[0] - depot_position[0],
    vehicle_position[1] - depot_position[1],
    vehicle_position[2] - depot_position[2],
]

print("Depot position:", depot_position)
print("Vehicle position:", vehicle_position)
print("Relative position:", relative_position)
```

## 6. Expected Output

```text
Depot position: [20, 10, 0]
Vehicle position: [100, 40, 5]
Relative position: [80, 30, 5]
```

## 7. Concept Check

This line:

```python
vehicle_position[0] - depot_position[0]
```

calculates the x component of the relative position.

This line:

```python
vehicle_position[1] - depot_position[1]
```

calculates the y component.

This line:

```python
vehicle_position[2] - depot_position[2]
```

calculates the z component.

## 8. Modification Exercise

Change the positions to:

```python
depot_position = [10, -5, 2]
vehicle_position = [25, 15, -3]
```

Calculate the relative position manually first.

Then run the code and see if it matches.

## 9. Short Quiz

Create this file:

```text
quizzes/000-foundation-bridge/003_relative_position.md
```

Answer:

1. What does relative position mean?
2. What does `r_rel` mean in plain English?
3. Why do we subtract depot position from vehicle position?
4. What is the relative position if `r_depot = [0, 0, 0]` and `r_vehicle = [5, 2, 1]`?
5. Why is relative position important for docking?

## 10. Completion Standard

You are done when:

- the Python file runs
- you can calculate relative position by hand
- you can explain why relative position is more useful than absolute position for docking
