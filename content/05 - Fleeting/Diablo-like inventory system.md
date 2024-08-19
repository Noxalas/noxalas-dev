---
draft: true
---
## Design requirements
- [x] Items as Resources.
- [x] Easy to add new items.
- [x] Non-rect shape for items must be possible.
- [ ] Drag-and-drop functionality that can easily be overridden. (Example: Custom drop area makes item drop in-world.) 

## User flow
```mermaid

style A color: #fff

flowchart TD
	A[Start] --> B(Initialize inventory)
	B --> C{Has user clicked on item?}
	C -->|Yes| D(Remove item from grid)
	C -->|No| E[Do nothing]
	D --> F(Place item in user's hand)
	F --> H{Has user dropped item?}
	H -->|Yes| I(Place item at grid position)

```