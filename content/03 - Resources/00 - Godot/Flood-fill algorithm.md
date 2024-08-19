---
title: Flood-fill algorithm
date: 2023-07-15
draft: true
description:
tags:
---
[[Algorithms]]

While I was working on a [[01 - Projects/Kaffestrig/Structure collapse system|structure collapse system]] similar to King Arthur's Gold, I had the need for an algorithm to step through tiles efficiently, and this is what I found.

```swift
func flood_fill(cell: Vector2i, max_dist: int) -> Array[Vector2i]:
	var array: Array[Vector2i]
	
	var stack := [cell]
	
	while not stack.is_empty():
		var current = stack.pop_back()
		
		var diff: Vector2i = (current - cell).abs()
		var dist: int = int(diff.x + diff.y)
		print(dist, " ", max_dist)
		if dist > max_dist:
			continue
		
		array.append(current)
		
		var used_cells: Array[Vector2i] = get_used_cells(0)
		var directions: Array[Vector2i] = [Vector2i.UP, Vector2i.DOWN, Vector2i.RIGHT, Vector2i.LEFT]
		for direction in directions:
			var coordinates: Vector2i = current + direction
			
			if not coordinates in used_cells:
				continue
			if coordinates in array:
				continue
			stack.append(coordinates)
	return array
```