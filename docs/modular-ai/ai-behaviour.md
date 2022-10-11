---
layout: default
title: AIBehaviour.cs
parent: Classes
grand_parent: Modular AI
---

# AIBehaviour.cs

## Description:
Contains conditions and actions that define behaviour.

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `string` | name |  | `"New Behaviour"` |
|  `List<BehaviourEvent>` | conditions |  |  |
|  `List<BehaviourEvent>` | actions |  |  |
|  `int` | threshold | The score theshold conditions need to reach for actions to execute (if behaviours are not competing). |  |

## Constructors:

| Summary      | Parameters | Returns |
|:------------------|:-----------|:--------|
|  | 'string' behaviourName, 'List<BehaviourEvent>' behaviourConditions, 'List<BehaviourEvent>' behaviourActions | `AIBehaviour` |
|  | 'string' behaviourName, 'List<BehaviourEvent>' behaviourConditions, 'List<BehaviourEvent>' behaviourActions, 'int' scoreThreshold | `AIBehaviour` |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| CompareTo |  | AIBehaviour other | `int` |
| checkCondition |  | `int` conditionIndex | `abstract Void` |
