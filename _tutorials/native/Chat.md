---
title: MCPE Native Mod Tutorial | Chat
permalink: /tutorials/native/chat/
shortname: Chat
---
In this particular tutorial, `game` is an instance of the `MinecraftGame` class. You can get this by overriding `MinecraftGame::onPlayerLoaded`, tutorial [here](http://pe.thediamondyt.tk/tutorials/native/events/player-loaded/). 

---

##### Mute chat
This function mutes or unmutes the chat. When the chat is muted, anything the player types wont be displayed in chat.
```cpp
game->getPrimaryGuiData()->toggleMuteChat();
```
