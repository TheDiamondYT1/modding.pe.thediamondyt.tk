---
title: MCPE Native Mod Tutorial | GUI
permalink: /tutorials/native/gui/display-message/
shortname: Displaying Messages
---
### Displaying messages
In this particular tutorial, `game` is an instance of the `MinecraftGame` class. You can get this by overriding `MinecraftGame::onPlayerLoaded`, tutorial [here](http://modding.pe.thediamondyt.tk/tutorials/native/events/player-loaded/). 
<br>
#### Client message
```cpp
game->getPrimaryGuiData()->displayClientMessage("Example text!");
```
<br>
#### Chat message
A message displayed in chat, displayed as `<player> text`.
```cpp
game->getPrimaryGuiData()->displayChatMessage("PlayerName", "Example text!");
```
<br>
#### Action bar message
A bar of small text displayed above the hotbar, but higher than a popup message.
```cpp
game->getPrimaryGuiData()->setActionBarMessage("Example text!");
```
<br>
#### Tip message
The same as an action bar message.
```cpp
game->getPrimaryGuiData()->displayTipMessage("Example text!");
```

---

##### You can also easily store the `GuiData` instance in a variable for easier use :)

```cpp
GuiData* gui = game->getPrimaryGuiData();
```
