---
title: MCPE Native Mod Tutorial | Init Game
permalink: /tutorials/native/events/init-game/
shortname: Init Game
---
This particular tutorial shows you how to do something when the game starts up.

```cpp
static void (*_Minecraft$init)(Minecraft*, bool);
static void Minecraft$init(Minecraft* self, bool unknown)
{
	_Minecraft$init(self, unknown);
	// do stuff here
}
```

Don't forget to hook it!

```cpp
MSHookFunction((void*) &Minecraft::init, (void*) &Minecraft$init, (void**) &_Minecraft$init);
```
