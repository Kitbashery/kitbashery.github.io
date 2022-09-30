---
layout: default
title: AIAgent.cs
parent: Classes
grand_parent: Modular AI
---

# AIAgent.cs

## Description:
Contains a list of behaviours that can be evaluated.

## Usage Notes:

An AI agent's behaviour loop is updated by an instance of `AIManager` if a manager instance is not found one will be created.

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `AIModule[]` | modules |  |  |
|  `bool` | modulesChanged | Has the amount of modules changed? | false |
|  `List<AIBehaviour>` | behaviours |  |  |
|  `UnityEvent` | preActionExecution | Events to be invoked before any behaviour actions are executed when `ExecuteWinningBehaviourActions()` is called. |  |
|  `UnityEvent` | postActionExecution | Events to be invoked after any behaviour actions are executed when `ExecuteWinningBehaviourActions()` is called. |  |
|  `bool` | debugMode | Toggles debug information in the console while in playmode. | false |
|  `DebugLevels` | debugLevel | How much information to log to the console while in debug mode. | DebugLevels.BehavioursOnly |
|  `ScoreTypes` | scoreType | The condition a behaviour's score needs to meet for its actions to execute. | ScoreTypes.HighestScoreWins |
|  `int` | scoreThreshold | The score a behaviour will need to beat in order for its actions to be executed. | 0 |
|  `bool` | hasBrokenReferences | Has a module that this agent depends on been removed? | false |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| UpdateAI |  |  | `Void` |
| ResetBehaviourEvaluation | Resets the initial score to beat and clears previously winning behaviours. Note: Call this if you change `scoreType` during runtime. |  | `Void` |
| ExecuteBehaviourActions |   | `AIBehaviour` behaviour | `Void` |
| AddNewEvent |   | `int` behaviourIndex, `BehaviourEvent` behaviourEvent | `Void` |
| ValidateBehaviours | Makes sure all components required by the behaviour logic has a component instance. |  | `Void` |
| FixBrokenReferences |  |  | `Void` |
| CheckForModuleChanges |  |  | `void` |


## Enumerations:

### DebugLevels

`{ All, BehavioursOnly, ConditionsOnly }`

### ScoreTypes

`{ AllScoresAboveThreshold, FirstScoreAboveThreshold, FirstScoreWins, HighestScoreWins, LowestScoreWins }`
