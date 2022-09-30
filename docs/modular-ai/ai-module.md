---
layout: default
title: AIModule.cs
parent: Classes
grand_parent: Modular AI
---

# AIModule.cs

## Description:
A base class for all AI modules.

## Usage Notes:

Components that inherit from this base class are automatically hidden in the editor. You cab prevent this by commenting out the `OnValidate() method:
```csharp
        private void OnValidate()
        {
            hideFlags = HideFlags.HideInInspector;
        }
```
Doing so will show modules as regular components in the inspector.
You may also wish to comment out the call to `DrawModules();` in the `OnInspectorGUI()` funciton in `AIAgentEditor.cs` this will prevent the custom module UI from being displayed.

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `abstract string[]` | conditions |  |  |
|  `abstract string[]` | actions |  |  |

## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| executeAction |  | `int` actionIndex | `abstract Void` |
| checkCondition |  | `int` conditionIndex | `abstract Void` |
