---
title: MCPE Native Mod Tutorial | Init Game
permalink: /tutorials/native/events/init-game/
shortname: Init Game
---
This particular tutorial shows you how to do something when the game starts up.

```cpp
static void (*_MinecraftGame$init)(MinecraftGame*);
static void MinecraftGame$init(MinecraftGame* self)
{
	_MinecraftGame$init(self);
	// do stuff here
}
```

Don't forget to hook it!

```cpp
MSHookFunction((void*) &MinecraftGame::init, (void*) &MinecraftGame$init, (void**) &_MinecraftGame$init);
```
