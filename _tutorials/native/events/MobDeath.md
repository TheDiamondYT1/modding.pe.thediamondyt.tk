---
title: MCPE Native Mod Tutorial | Mob Death
permalink: /tutorials/native/events/mob-death/
shortname: Mob Death
---
This particular tutorial shows you how to do something when a mob (such as a creeper) dies.
<br>
The equivalent ModPE method of this would be `deathHook(attacker, victim)`.

---

```cpp
static void (*_Mob$die)(EntityDamageSource*);
static void Mob$die(EntityDamageSource* source)
{
	_Mob$die(source);
	// do stuff here
}
```

Don't forget to hook it!

```cpp
MSHookFunction((void*) &Mob::die, (void*) &Mob$die, (void**) &_Mob$die);
```
