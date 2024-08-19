---
title: Kaffestrig Weekly -#1
date: 2023-07-29
draft: false
summary: First weekly update on all things Kaffestrig!
tags:
- post
- weekly
---
First weekly update on all things Kaffestrig!
If you don't know anything about the project, [[02 - Areas/Personal Dev Blog/Posts/Kaffestrig|you can read all about it here.]]

## IK Systems
![IK Image](99%20-%20Meta/01%20-%20Images/ik_stuff.gif)
*Yes, those are indeed KAG tiles.*

Most of this week was spent learning about and figuring out how to apply IK to my character animations, with varying amounts of success, but in the end I managed to get to a place where I'm happy enough that I can leave the legs be as they are for now.

The way I'm doing this is by:
- Using raycasts to place the feet on the ground.
- Offsetting the rays based on `Actor` movement, making it so we can control how far ahead the step targets are of the body. 
- Spinning the step targets on the feet based on the `Actor`'s movement. ([[Gait Controller]])
- Tracking the step targets with the actual IK targets, which the [[01 - Projects/notes/FABRIK|FABRIK]] nodes are reaching towards.

All in all, this gives me lots of flexibility and so *so* many different options on how to animate characters, since I've been fairly diligent in splitting all the concerns into smaller components.

Next up I'll be working on the hands, figuring out how to handle animation when a character equips items and weapons, and casts abilities through them.