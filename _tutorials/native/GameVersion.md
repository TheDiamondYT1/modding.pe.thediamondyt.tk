---
title: MCPE Native Mod Tutorial | Game Version
permalink: /tutorials/native/game-version/
shortname: Game Version
---
This tutorial simply shows you how to change the game version displayed on the title screen :)

One downside to this, however, is that your new version will be prefix with the letter `v`. This is fine for numerical versions, but if you were hoping for custom text then you should find a different way. 

---

```cpp
static std::string (*_Common$getGameVersionStringNet)();
static std::string Common$getGameVersionStringNet() {
   return "Hello world!";
}
```

Don't forget to hook it!

```cpp
MSHookFunction((void*) &Common::getGameVersionStringNet, (void*) &Common$getGameVersionStringNet, (void**) &_Common$getGameVersionStringNet);
```
