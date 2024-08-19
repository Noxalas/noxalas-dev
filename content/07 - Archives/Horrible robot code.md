---
draft: true
---

Some Java code I wrote while helping Tim.

```java

int directionsOpenCount;
boolean firstDirOpen;
boolean secondDirOpen;
boolean thirdDirOpen;
boolean fourthDirOpen;

for (int i = 0; i < 4; i++) {
	if (isFrontOpen()) {
		if (i == 0) firstDirOpen = true;
		if (i == 1) secondDirOpen = true;
		if (i == 2) thirdDirOpen = true;
		if (i == 3) fourthDirOpen = true;
		directionsOpenCount++;
	}
}

int randomOpenSpace = Utils.getRandomInt(0, directionsOpenCount);

int openSpaceCount = 0;
for (int i = 0; i < randomOpenSpace; i++) {
	if (firstDirOpen) {
		if (randomOpenSpace > openSpaceCount) {
			firstDirOpen = false;
			openSpaceCount++;
		}
		else {
			// move?
		}
	}
	else if (secondDirOpen) {
		if (randomOpenSpace > openSpaceCount) {
			firstDirOpen = false;
			openSpaceCount++;
		}
		else {
			// move?
		}
	}
	else if (thirdDirOpen) {
		if (randomOpenSpace > openSpaceCount) {
			firstDirOpen = false;
			openSpaceCount++;
		}
		else {
			// move?
		}
	}
	else if (fourthDirOpen) {
		if (randomOpenSpace > openSpaceCount) {
			firstDirOpen = false;
			openSpaceCount++;
		}
		else {
			// move?
		}
	}
}

```

```python

list openSpaces

for i in range(4):
	turn_left()
	if is_front_open():
		open_spaces.append(i)

int randomSpace = Utils.get_random_int(0, open_spaces.size())

for i in range(randomSpace):
	turn_left()

move()

```