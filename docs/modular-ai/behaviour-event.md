---
layout: default
title: BehaviourEvent.cs
parent: Classes
grand_parent: Modular AI
---

# BehaviourEvent.cs

### Implements:
`IComparable<BehaviourEvent>`

## Description:
Represents an action or condition that will be executed or evaluated by `AIAgent`.

## Usage Notes:
Contains two constructors one for defining the event as a condition and a shorter one to set the event as an action.

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:--------------------|:--------------|
|  `AIModule` | instance | The required module component instance that this event links to during runtime.|  |
|  `string` | moduleName | The assembly qualified name the required module instance. |  |
|  `int` | id | ID is the index of either an action or condition. |  |
|  `string` | name | The name of the event. |  |
|  `bool` | isCondition |  Does this event represent a condition? |  |
|  `int` | score | The score value of the event if the event represents a condition. |  |
|  `bool` | state | The required state of the event if the event represents a condition. |  |

## Constructors:
| Summary      | Parameters | Constructs |
|:--------------|:-----------|:--------|
| Constructs an event as a condition. | `string` eventName, `int` eventID, `AIModule` module, `int` conditionScore, `bool` conditionState | `BehaviourEvent` |
| Constructs an event as an action. | `string` eventName, `int` eventID, `AIModule` module | `BehaviourEvent` |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:--------------|:-----------|:--------|
| CompareTo | Required by IComparable. | `BehaviourEvent` other | `int` |
