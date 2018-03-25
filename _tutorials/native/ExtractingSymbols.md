---
title: MCPE Native Mod Tutorial | Extracting Symbols
permalink: /tutorials/native/extracting-symbols/
shortname: Extracting Symbols
---
This tutorial shows you how to extract symbols from `libminecraftpe.so` to create *most* headers. This method wont work for virtual methods, and you will need to use a tool like IDA Pro for that (but don't ask me how; i don't know).

You can do this on either Android 5.0 and above or on Linux. I'm not sure about Windows.

### Linux
1. Run `apt update && apt install binutils`.
2. See the "Extracting" section below.

<br>

### Android

1. Firstly, install [Termux](https://play.google.com/store/apps/details?id=com.termux) from the Google Play Store.
2. After its installed, run `apt update && apt install binutils`.
3. See the "Extracting" section below.

---

### Extracting
Firstly, extract an MCPE APK somewhere, and get the `libminecraftpe.so` file.

#### Getting all symbols
Run `nm -DC libminecraftpe.so`

<br>

#### Getting all methods in the "MinecraftGame" class
Run `nm -DC libminecraftpe.so | grep "MinecraftGame::"`

<br>

#### Getting all getters in the "MinecraftGame" class
Run `nm -DC libminecraftpe.so | grep "MinecraftGame::get"`

<br>

#### Getting all methods in the "GuiData" class
Run `nm -DC libminecraftpe.so | grep "GuiData::"`

<br>
You get the idea.