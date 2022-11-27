# C++ Portfolio
*See also: **[Lua Portfolio](lua-portfolio.md)***.

---

I've learned C++ in [Yandex.Practicum](https://practicum.yandex.ru/cpp/) course "C++ Developer" as additional professional education (2021-2022)
<img width="686" alt="Screenshot 2022-03-26 at 10 37 20" src="https://user-images.githubusercontent.com/5685050/160229778-e73b12d1-cef2-4619-8ab9-64e9339adf15.png">

I programmed for Linux, Arduino and modules with Lua C API.

# Code

## Yandex.Praktikum
### *https://github.com/GitSparTV/Yandex.Practicum.CPP*

<img src="https://github.com/GitSparTV/Yandex.Practicum.CPP/raw/master/TransportCatalogue/svg.png">

Projects I made during Yandex.Praktikum "C++ Developer" course.

The course teaches C++ fundamentals and idioms, from basic logic up to multithreading, move semantics, remaking STL containers, making lexers and ASTs and more.

See **11** more showcases on the repo page.

## University admission watcher
### *https://github.com/GitSparTV/Files/tree/master/AdmissionWatcher*

<img width="555" src="https://user-images.githubusercontent.com/5685050/204158820-5daf5d6a-02fc-464a-bb3d-6aeea535f4b4.png">

For my wife and a friend I created a Telegram bot, that fetches the changes in admission lists and compares the last version with the new one.

The differences are reported to telegram channel. Even though I've had not much time to make the bot while it's still relevant, I followed code style, C++ idioms and DRY concept.

## Contractor
### *https://gist.github.com/GitSparTV/4f122876ca1ead0ef04f4d9bdc489f61*

Multithreaded task splitter.

Contractor has one function and one work type. Each worker gets work from the queue.

Was used to compute `n!` algorithm efficiency.

## globalize
### *https://github.com/GitSparTV/globalize*

Simple C program that installs other program to /usr/local/bin/. Uses Linux API.

# Lua C API
## lmemprof
### *https://github.com/GitSparTV/lmemprof*

Lua and LuaJIT library to profile memory consumption written in C++.

Currently, just hooks into allocator using lua_setallocf.

New concept will dump what structure exactly are sitting in the memory (like tables, strings, etc.).

## RemPos
### *https://github.com/GitSparTV/gmsv_rempos*

https://user-images.githubusercontent.com/5685050/143723137-593afe00-7c64-4690-87ab-0fe94f25c7de.mp4

Garry's Mod C++ module written with websocketpp for iOS app Senzor app (by Stanislav Révay).

iOS app reads device accelerometer, gyroscope and GPS and pressure data and sends it to the websocket server open by module.

Server stores latest data packet and exposes getters to Lua guarded by mutex.

## LuaWheel
### *https://github.com/GitSparTV/LuaWheel*

<img src="https://github.com/GitSparTV/LuaWheel/raw/master/LuaWheelDemo.gif">

Lua module written in C++ with Logitech Wheel SDK.

Allows to get all parameters and fully control Logitech wheel.

## LuaCUE
### *https://github.com/GitSparTV/LuaCUE*

https://user-images.githubusercontent.com/5685050/142698638-164dd8ae-3e4f-4198-b3af-a210abdf9e74.mp4

App with Lua runtime with preloaded module for communicating with iCUE SDK (Corsair mice and keyboards).

[![HitCount](http://hits.dwyl.com/GitSparTV/cpp-portfolio.svg?style=flat)](http://hits.dwyl.com/GitSparTV/cpp-portfolio)
