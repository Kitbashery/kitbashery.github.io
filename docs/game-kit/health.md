---
layout: default
title: Health.cs
parent: Classes
grand_parent: Game Kit
---

# Health.cs

## Description:
Tracks "hit points" and invokes events based on the current amount or state.

## Usage Notes:

Bonus Health should not be set to its own `health` component.

Tip: Lowercase fields in the inspector can be set via UnityEvents.
 

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `bool` | invinsible |  | `false` |
|  `Health` | bonusHealth | If assigned the hitpoints of the bonus health will need to be depleted before damage can be applied to this health component. |  |
|  `int` | hitPoints | The hitpoints to start with, it isn't recommended to modify this value directly during runtime, use ModifyHealth() instead. | 100, Minimum value = 0 |
|  `bool` | overhealExpand | Should the maximum hit points be expanded if healed beyond maxHitPoints? | false |
|  `bool` | canRegen | Enables passive health regeneration. | false |
|  `int` | regenPoints | Hitpoints to regenerate. | 1, Minimum value = 1 |
|  `float` | regenRate | Time between regenerating hitpoints (in seconds). | 0.1, Minimum value = 0.01 |
|  `UnityEvent` | onReceivedDamage |  |  |
|  `UnityEvent` | onHealed |  |  |
|  `UnityEvent` | onDead |  |  |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| ModifyHealth |  | HealthModifiers modifier, int amount | `Void` |
| ModifyHealthOverTime   | Starts a `TimedHealthEffect` that will modify health over time. | `TimedHealthEffect` effect | `Void` |
| StopTimedEffectsWithModifier |  Stops all timed health effects that use a specific health modifier.  | `HealthModifiers` modifier | `Void` |
| StopTimedHealthEffect | Stops a specific health effect by its `TimedHealthEffect` name.  | `string` effectName | `Void` |
| StopAllTimedHealthEffects |  |  | `Void` |
| ApplyDamage | Applies damage, if there is bonus health damage will be applied to that component first. | `int` amount "The amount of damage to apply". | `Void` |
| ClearRegenCooldown | Instantly regenerates hitpoints if canRegen is true. |  | `void` |
| Heal | Instantly heals the specified amount of hitpoints. | `int` amount "The amount of hitpoints to heal". | `void` |
| ResetHealth | Resets the hitpoints of all health and (optionally) all bonus health components in the chain to their original values. Useful for pooling. | `bool` resetBonusHealth "If true will reset the bonus health recursively until no bonus health is found." Default value = `false` | `Void` |
| SetMaxHitpoints | Overrides the initial hitpoint value and adjusts the current hitpoints to fit within the new range. | `int` amount "The new max value of hitpoints". | `void` |
| IsLessThanHalfHealth | Checks if the amount of hitpoints is below 50% of the intial value. | | `bool` "true if hitpoints are below 50%". |
| TimedEffectsPlaying | Checks if there are any heal/damage over time effects being apllied. |  | `bool` "true if there are effect playing". |
| HasTimedHealthEffect | Checks if there is a specific timed health effect playing. | `string` effectName "The name of the effect to check for". | `bool` "true if an effect is found". |
| DebugTimedEffectCount |  |  | `void` |
| DebugCurrentHealth |  |  | `void` |


## Structs:

### `[Serializable]` TimedHealthEffect
#### Public Properties:

| Type        | Name | Description | Default Value |
|:------------|:----|:-------------|:--------------|
|  `string` | name | The name of the effect, used for stopping effects with this name. |  |
|  `int` | amount | The amount of healing or damage to apply. | Minumum value = 1 |
|  `int` | times | The amount of times to modify health. | Minumum value = 1 |
|  `float` | interval | Time interval in seconds between modifying health. | Minumum value = 0 |

## Enumerations:

### HealthModifiers

`{ damage, heal }`
