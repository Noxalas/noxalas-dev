---
title: Ability casting targets
date: 2023-07-23
draft: true
description:
tags:
---

We have a couple ways we could get the casting targets to fire off spells:
1. Let the casting targets connect to the `ability_activated` signal and fire off the spell as well, somehow giving the spell information about the target's location and rotation.
	- Issue here is that we have to stop the spell from firing in the `AbilityContainer` itself.
2. We could also let the `AbilityContainer` itself manage casting targets, creating an export array of them, and if the array isn't empty the container stops its own cast and iteratively casts on each target.

I ended up making the targets assign themselves to the `AbilityContainer` automatically, then when an ability is cast an array of all the targets is bundled with the `ActivationEvent`. The ability can do whatever it likes with the array like, for example, casting multiple projectiles. 

















| Name |       |     |     |
| ---- | ----- | --- | --- |
|      |       |     |     |
|      | This  |     |     |
|      | Hello |     |     |
|      |       |     |     |
|      |       |     |     |







