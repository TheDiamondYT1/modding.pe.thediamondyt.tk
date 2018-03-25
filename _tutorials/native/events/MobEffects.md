---
title: MCPE Native Mod Tutorial | Mob Effects
permalink: /tutorials/native/events/mob-effects/
shortname: Mob Effects
---
This particular tutorial shows you how to do stuff when mob effects are added or removed.

---

### Effect Added

```cpp
static void (*_Mob$onEffectAdded)(MobEffectInstance*);
static void Mob$onEffectAdded(MobEffectInstance* effect)
{
    _Mob$onEffectAdded(effect);
    // do stuff here
}
```

Don't forget to hook it!

```cpp
MSHookFunction((void*) &Mob::onEffectAdded, (void*) &Mob$onEffectAdded, (void**) &_Mob$onEffectAdded);
```
