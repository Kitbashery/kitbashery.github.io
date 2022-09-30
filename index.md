---
layout: default
title: Home
nav_order: 1
description: "Kitbashery description placeholder."
permalink: /
---
![](https://kitbashery.com/assets/images/kitbashery-github-banner.jpg)

<b>Kitbashery professionally develops & maintains a collection of Unity assets as a freemium service.</b>

## Why Freemium?

<p>
<b>After years of working in Unity with thousands of dollars invested
in the Unity Asset Store both as a publisher and consumer I found that:</b>
</p>
<ul>
<li>It is unsustainable for most asset publishers to offer unlimited free suport and feature updates for life.</li>
<li>The consumer could receive a broken, unsupported or close source asset no matter the inital price tag.</li>
<li>Paid upgrades split the user base and don't have a "try before you buy" option.</li>
<li>Updates to assets could take weeks to months for the asset store's review process to complete.</li>
</ul>

### Benefits of freemium:

<ul>
<li>Assets are free of an initial charge. No more paying for expensive broken assets you can't refund.</li>
<li>If you like the asset then you can tip or pay what you want later.</li>
<li>Assets & documentation are open-source and can be maintained in case the main developer suddenly kicks the bucket.</li>
<li>Long term maintenance and support funded via a crowdfunding subscription model.</li>
<li>Feature requests/new assets are developed on a per commission basis (or added by the community).</li>
<li>The latest version is always available to download.</li>
</ul>

## Installation Options:
<ol>
<li>The Unity Asset Store will have packages for the current Unity LTS version.</li>
<li>The most recent version can be downloaded from the asset's product page on <a href="https://kitbashery.com/">kitbashery.com</a>.</li>
<li>Legacy versions can be found in the asset's GitHub repository's Releases tab.</li>
<li>Assets can be downloaded from Kitbashery's Ko-Fi store for free or you can "pay what you want".</li>
<li>Copy the asset's GitHub repository's Clone HTTPS URL and paste it into the package manager.</li>
<li>Install via openUPM (click the badge on the asset's GitHub repo).</li>
</ol>

## Contributing:
All code contributions are subject to the following requirements:

<p>
All C# code must be up to Microsoft's <a href="https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions">C# Coding Conventions</a>. In the past Unity used conventions like using m_variableName and such practices can still be found in legacy code. However going forward Microsoft's conventions are now the standard.
</p>

In addition to the C# coding standards there is a preferred comment and region structure to follow.

<li>Encapsulate all properties in a #region labeled: Properties:</li>
<li>Encapsulate all Monobehaviour Initializers, Updates, Gizmos and IEnumerators in a #region labeled: Initialization & Updates.</li>
<li>Encapsulate Methods in a #region labeled: Methods: within this region you can have sub regions labeled to your liking.</li>
<li>Triple slash summary comments must be used on all public methods and properties that are not obviously named. These summary comments correlate to the descriptions in the documentation.</li>


```csharp
///<summary>
/// your summary...
///</summary>
YourMethod()
{
  //your code.
}
```
Sometimes when there is a private field/method that isn't very well named it is a good idea to add a summary comment there as well.

Additionally over any public property field that will be displayed in Unity's inspector window include:


```csharp 
[ToolTip("Your tooltip text")]
```

Sometimes with very obviously named fields that are self explanatory it isn't necessary to add a tooltip attribute, but in most cases it is preferred.

In some cases it is prefered to be more strict than Microsoft's conventions such as var is rarely if ever used, instead a known type should be used. Additionally when checking if statements == true/false is always used instead of if(variableName) These two practices are done to reduce ambiguity.

After putting in a pull request it is helpful (but not necessary) to also document them by putting in a pull request to The documentation repo and update the docs. Doing so however does not mean your additions/changes will be accepted so it may be best to add docs after your changes have been merged or let an official developer document the changes.

Code that deviates to far from these guidelines may not be merged untill it is revised and/or fits within the scope of the project.
