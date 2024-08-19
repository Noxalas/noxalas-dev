---
draft: true
---
[[01 - Projects/Nimbus Nook/Project Nimbus|Project Nimbus]]
## Engine choice
The Godot Engine is a versatile and very simple game engine that is well suited for indie developers developing both 2D and 3D games. 
## Feature List


## Software List
### Godot
Game engine and IDE.
### Git
Source control
### Aseprite
Main art program used by the team. 
### Blender 
Modeling software.

## High Level Diagrams

## Assets
The game's resources are categorized like this:
- Actors
- Models
- Materials
- Shaders
- Textures
- Dialogues

## Game Logic & AI

## Release Platforms
PC & Linux, with the possibility of macOS and consoles (Switch, PlayStation & Xbox), but with certain additional requirements (SDKs and contracts).

## Hardware Requirements
A system supporting Vulkan is preferred due to the nature of Godot 4.x using Vulkan heavily, but support for OpenGL 3 could be supplied through an additional export
## Rendering
### Stylistic choice of pixelization

## "Quest" System
Quests are more like accomplishments. Anything a designer would like to track that the player has done is a "quest" handled by a simple tag system. These tags can be checked elsewhere to control the state of other parts of the game. 

A simple example might be "player_seen_intro" where, if the tag exists, the intro will not play again.