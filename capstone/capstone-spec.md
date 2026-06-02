# Capstone Specification

## Capstone Name

Autonomous Depot Network Simulator

## Purpose

Build a simulation and analysis system for reasoning about depot-based autonomous space logistics infrastructure.

This capstone is not intended to prove a final spacecraft design. It is intended to develop engineering judgment, simulation skill, systems thinking, and evidence artifacts.

## Final Deliverables

1. Depot network simulator
2. Technical white paper
3. Requirements and verification matrix
4. Trade study memos
5. Failure-mode simulation cases
6. Visual diagrams/results
7. Final portfolio summary

## Simulator Scope

The simulator should eventually represent:

- depot nodes
- spacecraft or cargo vehicles
- transfer paths
- state vectors
- time and mission phases
- resource constraints
- propellant or delta-v budgets
- communication assumptions
- depot availability
- failure states
- autonomous decision logic
- telemetry and anomaly signals

## Initial Minimum Viable Simulator

The first version only needs:

- nodes with positions
- edges with cost/time attributes
- simple vehicle state
- route comparison
- basic failure injection
- output summary table

## Advanced Simulator Targets

Later versions should include:

- orbital mechanics approximations
- uncertainty propagation
- Monte Carlo cases
- GNC-inspired control logic
- station-keeping assumptions
- depot health state
- autonomous maintenance tasks
- telemetry anomaly detection
- report generation

## White Paper Structure

1. Executive technical summary
2. Problem statement
3. Depot-network hypothesis
4. System architecture
5. Simulation model
6. Assumptions and limitations
7. Results
8. Risks and failure modes
9. Verification approach
10. Future work

## Capstone Rule

Every module should move the capstone forward either by adding code, analysis, a technical memo, or a verified model assumption.
