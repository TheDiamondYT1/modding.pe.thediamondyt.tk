---
title: MCPE Native Mod Tutorial | GUI
permalink: /tutorials/native/gui/display-message/
shortname: Displaying Messages
---
### Displaying messages
In this particular tutorial, `game` is an instance of the `MinecraftGame` class.

##### Client message
```
sel->getGuiData()->displayClientMessage("Example text!");
```

##### Chat message
A message displayed in chat, displayed as `<player> text`.
```
game->getGuiData()->displayChatMessage("PlayerName", "Example text!");
```

##### Action bar message
A bar of small text displayed above the hotbar, but higher than a popup message.
```
game->getGuiData()->setActionBarMessage("Example text!");
```

##### Tip message
The same as an action bar message.
```
game->getGuiData()->displayTipMessage("Example text!");
```
