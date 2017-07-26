---
title: MCPE Native Mod Tutorial | Edu Mode
permalink: /tutorials/native/cool-things/enable-edu-mode/
shortname: Edu Mode
---
So we've all heard about Minecraft: Education Edition, and heard that it's only available for schools. Not any more! 
With this cool trick you can get the general feel of the special edition of Minecraft.

---

```cpp
static bool (*_MinecraftGame$isEduMode)();
static bool MinecraftGame$isEduMode()
	return true;
}
```

Don't forget to hook it!

```cpp
MSHookFunction((void*) &MinecraftGame::isEduMode, (void*) &MinecraftGame$isEduMode, (void**) &_MinecraftGame$isEduMode);
```
