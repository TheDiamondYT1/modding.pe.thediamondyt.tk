---
title: MCPE Native Mod Tutorial | GUI
permalink: /tutorials/native/gui/display-message/
shortname: Displaying Messages
---
### Displaying messages
In this particular tutorial, `game` is an instance of the `MinecraftGame` class.  
<br>
#### Client message
```cpp
game->getGuiData()->displayClientMessage("Example text!");
```
<br>
#### Chat message
A message displayed in chat, displayed as `<player> text`.
```cpp
game->getGuiData()->displayChatMessage("PlayerName", "Example text!");
```
<br>
#### Action bar message
A bar of small text displayed above the hotbar, but higher than a popup message.
```cpp
game->getGuiData()->setActionBarMessage("Example text!");
```
<br>
#### Tip message
The same as an action bar message.
```cpp
game->getGuiData()->displayTipMessage("Example text!");
```
