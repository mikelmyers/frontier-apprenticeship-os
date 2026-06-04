# Lesson 006 — Day One Review: Depot Approach Snapshot

## Objective

Combine the first five concepts into one small depot approach snapshot.

You will calculate:

- relative position
- relative velocity
- distance / magnitude

This is the first small version of approach monitoring.

## 1. Plain-English Scenario

A depot is sitting at one position.

A vehicle is nearby at another position.

The depot has a velocity.

The vehicle has a velocity.

We want to answer:

1. Where is the vehicle relative to the depot?
2. How far away is the vehicle?
3. How fast is the vehicle moving relative to the depot?

## 2. Concepts Used

```text
r_depot      = depot position
r_vehicle    = vehicle position
r_rel        = vehicle position relative to depot
||r_rel||    = distance between vehicle and depot
v_depot      = depot velocity
v_vehicle    = vehicle velocity
v_rel        = vehicle velocity relative to depot
```

## 3. Python Implementation

Create this file:

```text
exercises/000-foundation-bridge/006_day_one_review.py
```

Type this manually:

```python
import math

depot_position = [20, 10, 0]
vehicle_position = [100, 40, 5]

depot_velocity = [0, 0, 0]
vehicle_velocity = [-2, -1, 0]

relative_position = [
    vehicle_position[0] - depot_position[0],
    vehicle_position[1] - depot_position[1],
    vehicle_position[2] - depot_position[2],
]

relative_velocity = [
    vehicle_velocity[0] - depot_velocity[0],
    vehicle_velocity[1] - depot_velocity[1],
    vehicle_velocity[2] - depot_velocity[2],
]

x = relative_position[0]
y = relative_position[1]
z = relative_position[2]

distance = math.sqrt(x**2 + y**2 + z**2)

print("Relative position:", relative_position)
print("Relative velocity:", relative_velocity)
print("Distance:", distance)
```

## 4. Expected Output

```text
Relative position: [80, 30, 5]
Relative velocity: [-2, -1, 0]
Distance: 85.58621384311844
```

## 5. Deeper Concept Explanation

This is not yet a full simulation. It is a snapshot.

A snapshot tells us what is true at one moment.

A simulation tells us how the system changes over many moments.

Today, we are only doing the snapshot.

Later, a loop will repeat this calculation over and over across many time steps.

That is how simple code becomes a simulation.

## 6. Modification Exercise

Add this safety rule:

```text
If distance is greater than 100, print "Vehicle is far."
If distance is between 20 and 100, print "Vehicle is in approach zone."
If distance is less than 20, print "Vehicle is in close operations zone."
```

Hint:

```python
if distance > 100:
    print("Vehicle is far.")
elif distance >= 20:
    print("Vehicle is in approach zone.")
else:
    print("Vehicle is in close operations zone.")
```

## 7. Short Quiz

Create this file:

```text
quizzes/000-foundation-bridge/006_day_one_review.md
```

Answer:

1. What is the difference between position and relative position?
2. What is the difference between velocity and relative velocity?
3. What does `||r_rel||` mean?
4. Why is this lesson a snapshot and not yet a simulation?
5. What would need to be added to turn this into a simulation?
6. What part of Day One still feels unclear?

## 8. Completion Standard

You are done when:

- the review file runs
- you added the safety rule
- you answered the quiz
- you can explain the difference between a snapshot and a simulation
