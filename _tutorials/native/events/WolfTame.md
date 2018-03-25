---
title: MCPE Native Mod Tutorial | Wolf Tame
permalink: /tutorials/native/events/wolf-tame/
shortname: Wolf Tame
---
This particular tutorial shows you how to do something when a wolf becomes tamed.

---

```cpp
static void (*_Wolf$onTame)();
static void Wolf$onTame()
{
    _Wolf$onTame();
    // do stuff here
}
```

Don't forget to hook it!

```cpp
MSHookFunction((void*) &Wolf::onTame, (void*) &Wolf$onTame, (void**) &_Wolf$onTame);
```
