---
layout: default
title: Getting Started
parent: Modular AI
nav_order: 1
has_children: true
---

# Getting Started:
To get started using Modular AI first create a GameObject with an AIManager component.

All Modular AI components can be found through the component menu:

![](../../assets/images/kitbashery-modular-ai-component-navigation.jpg)

Next create a new GameObject with an AIAgent component and add the modules you want to it.

Modules contain code that defines behaviour logic the AI can use & can be configured using the inspector.

## Utility Theory:

Modular AI uses utility theory for its AI behaviour logic. An AI agent can have as many behaviours as you want.

### Behaviours:
Behaviours are comprised of conditions and actions and have a score value. The behaviour with the score that best meets the criteria you set will execute its actions.
### Conditions:
Conditions are true/false statements based on what the AI knows about the game world. If a condition meets its desired state the it will add its score to the behaviour's total score.
### Actions:
Actions are executed in the order they are arranged if a behaviour's score wins.


![](../../assets/images/kitbashery-modular-ai-agent-component.jpg)
