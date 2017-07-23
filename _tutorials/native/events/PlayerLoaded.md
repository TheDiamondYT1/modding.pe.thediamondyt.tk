---
title: MCPE Native Mod Tutorial | Player Loaded
permalink: /tutorials/native/events/player-loaded/
shortname: Player Loaded
---
This particular tutorial shows you how to do something when a player joins the level.

```cpp
static void (*_MinecraftGame$onPlayerLoaded)(MinecraftGame*, Player&);
static void MinecraftGame$onPlayerLoaded(MinecraftGame* self, Player& player)
{
	_MinecraftGame$onPlayerLoaded(self, player);
	// do stuff here
}
```

Don't forget to hook it!

```cpp
MSHookFunction((void*) &MinecraftGame::onPlayerLoaded, (void*) &MinecraftGame$onPlayerLoaded, (void**) &_MinecraftGame$onPlayerLoaded);
```
