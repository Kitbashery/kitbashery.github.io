---
layout: default
title: TimeManager.cs
parent: Classes
grand_parent: Game Kit
---

# TimeManager.cs

## Description:
Manages play/pause, framerate events and time scale effects.

## Usage Notes:

Bonus Health should not be set to its own `health` component.

Tip: Lowercase fields in the inspector can be set via UnityEvents.
 

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `static TimeManager` | Instance |  |  |
|  `KeyCode` | togglePauseKey |  | KeyCode.Escape |
|  `bool` | pauseAudio |  | true |
|  `bool` | pauseTime |  | true |
|  `bool` | showCursor |  | true |
|  `UnityEvent` | onPause |  |  |
|  `UnityEvent` | onUnPause |  |  |
|  `bool` | modifyingTimeScale |  | false |
|  `float` | currentTimeDuration |  | 0 |
|  `float` | currentTimeMultiplier |  | 0 |
|  `bool` | debugFps | Should fps counters be updated and fps events invoked? | false |
|  `Text` | fpsCounter |  |  |
|  `TMP_Text` | fpsCounterTMP |  |  |
|  `float` | targetFPS |  | 60, Minimum Value = 1 |
|  `float` | currentFPS |  |  |
|  `UnityEvent` | onBelowTargetFPS |  |  |
|  `UnityEvent` | onAboveTargetFPS |  |  |


## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| CountFPS |  |  | `Void` |
| DebugFPS   |  |  | `Void` |
| ScaleTime | Scales the time of the game for the specified duration.  | `float` multiplier "How much to add to the timescale.", 'float` duration "The duration of the effect.", `bool` addMultiplier "Should the current multiplier be added onto.", `bool` addDuration "Should the current durration be added onto." | `Void` |
| StopTimedHealthEffect | Stops a specific health effect by its `TimedHealthEffect` name.  | `string` effectName | `Void` |
| SlowMoHalfSpeed | Slows the time scale to half speed (overrides ScaleTime effects). | `float` duration "How long the slow motion effect lasts." | `Void` |
