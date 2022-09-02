---
layout: default
title: MemoryModule.cs
parent: Classes
grand_parent: Modular AI
---

# MemoryModule.cs

### Inherits from:
[AIModule.cs](https://kitbashery.com/docs/modular-ai/ai-module.html)

## Description:
This module contains actions and condtions to remember `GameObject`s and `AIAgent`s that it has been made aware of in the environment.

## Usage Notes:

The tags "Player" and "Agent" are used by this module by default make sure they exist in your project settings if you use them.

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `List<GameObject>` | objects |  |  |
|  `List<AIAgent>` | agents |  |  |
|  `List<GameObject>` | players |  |  |
|  `GameObject` | objectFocus |  |  |
|  `AIAgent` | agentFocus |  |  |
|  `GameObject` | playerFocus |  |  |
|  `string` | focusTag |  |  |
|  `string` | agentTag |  | "Agent" |
|  `string` | playerTag |  | "Player" |


## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| FocusOnGameObject |  | `FocusModes` focusMode | `Void` |
| FocusOnAgent |  | `FocusModes` focusMode | `Void` |
| FocusOnPlayer |  | `FocusModes` focusMode | `Void` |
| AddObjectToMemory |  | `GameObject` go | `Void` |
| AddAgentToMemory |  | `AIAgent` agent | `Void` |
| FindAgentsInEnvironmentMemory | Finds all `AIAgent`s in `objects` and moves them to `agents`. |  | `Void` |
| FindPlayersInEnvironmentMemory | Finds all GameObjects tagged as a player in `objects` and moves them to `players`. |  | `Void` |


## Enumerations:

### FocusModes

`{ Nearest, Farthest, Random, First, Last }`
