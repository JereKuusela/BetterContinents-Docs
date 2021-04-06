---
layout: default
title: Ridges
parent: Settings
nav_order: 9
---

# Ridges
{: .no_toc }

Ridges are an extra layer of procedural noise generation (i.e. not using an image, but calculated "randomly" instead) you can introduce into the height generation that have a "ridged" and/or "warped" appearance. This can give quite interesting and realistic topology, roughly emulating folding, or the collision of tectonic plates.

<details open markdown="block">
<summary>
Contents
</summary>
{: .text-delta }
1. TOC
{:toc}
</details>

## Max Ridge Height
{: .d-inline-block }
Setting
{: .label .label-green }

Max height of ridge features (set this to 0 to turn OFF ridges entirely).
> Default `0.5`  
> Range `0` to `1`

<details class="console" markdown="block">
<summary>
Console
</summary>
Command: `bc param ri mh`
<img src="../images/console/bc-param-ri-mh.gif" />
</details>

## Ridge Size
{: .d-inline-block }
Setting
{: .label .label-green }

Size of ridge features.
> Default `0.5`  
> Range `0` to `1`

<details class="console" markdown="block">
<summary>
Console
</summary>
Command: `bc param ri si`
<img src="../images/console/bc-param-ri-si.gif" />
</details>

## Ridge Blend
{: .d-inline-block }
Setting
{: .label .label-green }

Smoothness of ridges blending into base terrain.
> Default `0.5`  
> Range `0` to `1`

<details class="console" markdown="block">
<summary>
Console
</summary>
Command: `bc param ri bl`
<img src="../images/console/bc-param-ri-bl.gif" />
</details>

## Ridge Amount
{: .d-inline-block }
Setting
{: .label .label-green }

How much ridges.
> Default `0.5`  
> Range `0` to `1`

<details class="console" markdown="block">
<summary>
Console
</summary>
Command: `bc param ri am`
<img src="../images/console/bc-param-ri-am.gif" />
</details>
