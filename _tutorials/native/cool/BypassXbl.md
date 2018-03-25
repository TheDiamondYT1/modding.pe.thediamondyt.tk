---
title: MCPE Native Mod Tutorial | Bypass Xbox Live
permalink: /tutorials/native/cool-things/bypass-xbl/
shortname: Bypass XBL
---
This does require you to not have an xbox live account saved at all however, so it might be a good idea to wipe BlockLauncher's data first.

---

```cpp
static bool (*_XboxLiveUserManager$isSignedIn)();
static bool XboxLiveUserManager$isSignedIn()
{
    return true;
}

static bool (*_ServiceClient$isSignedIntoXboxLive)();
static bool ServiceClient$isSignedIntoXboxLive()
{
    return true;
}
```

Don't forget to hook it!

```cpp
MSHookFunction((void*) &Social::XboxLiveUserManager::isSignedIn, (void*) &XboxLiveUserManager$isSignedIn, (void**) &_XboxLiveUserManager$isSignedIn);
MSHookFunction((void*) &ServiceClient::isSignedIntoXboxLive, (void*) &ServiceClient$isSignedIntoXboxLive, (void**) &_ServiceClient$isSignedIntoXboxLive);
```
