---
layout: default
title: MAI_EditorUtility.cs
parent: Classes
grand_parent: Modular AI
---

# MAI_EditorUtility.cs

## Description:
Utility class for drawing commonly used editor GUI elements for modular AI's custom inspectors.

## Public Properties:

| Type        | Name | Description         | Default Value |
|:-------------|:----|:------------------|:------|
|  `static GUIStyle` | centeredBoldHelpBox |  |  |
|  `static GUIStyle` | wrappedMiniLabel |  |  |
|  `static GUIStyle` | miniLabel |  |  |
|  `static GUIStyle` | centeredMiniLabel |  |  |
|  `static GUIStyle` | upperLeftMiniLabel |  |  |
|  `static GUIStyle` | centeredLabel |  |  |
|  `static GUIStyle` | centeredBoldLabel |  |  |
|  `static GUIStyle` | middleLeftBoldLabel |  |  |
|  `static GUIStyle` | lowerLeftBoldLabel |  |  |
|  `static GUIStyle` | clippingBoldLabel |  |  |
|  `static GUIStyle` | rightAlignedLabel |  |  |
|  `static GUIStyle` | richText |  |  |
|  `static GUILayoutOption[]` | horizontalLine |  |  |
|  `static GUILayoutOption[]` | thickHorizontalLine |  |  |


## Public Methods:

| Name | Summary      | Parameters | Returns |
|:----|:------------------|:-----------|:--------|
| DrawHelpTitleToggle | Draws a bold title with a help button that toggles a help box. Useage example: `myBool = DrawHelpTitleToggle(myBool, "title", "message");` | `bool` toggle "Boolean to pass in and return.", `string` title "Text for the bold title.", `string` text "Text for the help box to display." | `static bool` "Returns toggle" |
| DrawFoldout |  | `bool` value, `string` label | `static bool` |
| DrawCompactPopup |   | `string` label, `int` value, `string[]` options | `static int` |
| DrawComponentOptions |   | `Component` component | `static Void` |
