---
layout: default
title: AIManager.cs
parent: Classes
grand_parent: Modular AI
---

# AIManager.cs

## Description:
Consolidates `AIAgent` update loops improving performance.

## Usage Notes:
 
* Default script execution order is -21 to load before AIAgents.cs.
 

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `static AIManager` | Instance |  |  |
|  `List<AIAgent>` | agents |  |  |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| Register |  | `AIAgent` agent | `Void` |
| Unregister |  | `AIAgent` agent | `Void` |
