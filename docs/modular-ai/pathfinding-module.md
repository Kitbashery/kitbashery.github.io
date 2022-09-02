---
layout: default
title: PathfindingModule.cs
parent: Classes
grand_parent: Modular AI
---

# PathfindingModule.cs

### Inherits from:
[AIModule.cs](https://kitbashery.com/docs/modular-ai/ai-module.html)

## Description:
Module that defines actions and conditions for a `AIAgent` to pathfind using Unity's built-in `NavMeshAgent`.

## Usage Notes:

An AI agent's behaviour loop is updated by an instance of `AIManager` if a manager instance is not found one will be created.

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `bool` | debugMode | Toggles debug mode for displaying gizmos when the agent is selected. | false |
|  `NavMeshAgent` | agent |  |  |
|  `Transform` | target | The target location for the agent to pathfind to. |  |
|  `MemoryModule` | memory |  |  |
|  `PatrolRoute` | patrolRoute | Positions representing a patrol route in the order they should be navigated to. |  |
|  `float` | fleeDistance | How far the agent should flee from a target. | 16 |
|  `float` | followDistance | How far from a target the agent need to be to follow it. | 4 |
|  `float` | wanderRange | How far can this agent wander? | 4 |
|  `float` | wanderTime | How long the agent should wait until it wanders again. | 1.5f, Minimum Value = 0 |
|  `float` | patrolWaitTime | The time the agent waits before moving to the next waypoint. | 0 |
|  `int` | timesToPatrol | How many times the agent should patrol though its waypoint route. (0 = forever) | 0 |
|  `PatrolTypes` | patrolType |  | 0 |
|  `int` | timesPatroled |  | PatrolTypes.loop |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| Flee |  |  | `Void` |
| FollowTarget | |  | `Void` |
| Idle |   |  | `Void` |
| MoveToTarget |   |  | `Void` |
| StopPatrol |  |  | `Void` |
| Patrol |  |  | `Void` |
| Wander |  |  | `void` |


## Enumerations:

### PatrolTypes

`{ loop, pingPong, randomize }`
