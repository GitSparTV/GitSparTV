# C++ Portfolio
*See also: **[Lua Portfolio](lua-portfolio.md)***.

---

I'm learning C++ in [Yandex.Praktikum](https://practicum.yandex.ru/cpp/) course "C++ Developer" as additional professional education since Feb 2021 (Will graduate in Jan 2022).

I also coded a Linux program, Arduino programs and modules with Lua C API.

# Code

## Yandex.Praktikum
### *https://github.com/GitSparTV/Yandex.Practicum.CPP*

<img src="https://github.com/GitSparTV/Yandex.Practicum.CPP/raw/master/TransportCatalogue/svg.png">

Projects I was making during Yandex.Praktikum "C++ Developer" course.

The course teaches C++ fundamentals and idiomatics, from basic logic up to multithreading, move semantics, remaking STL containers and more.

To see more information, see the repo page.

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

Garry's Mod C++ module written with evhttp (libevent) for Sensor Logger app for iOS (app got deleted).

iOS app reads device accelerometer, gyroscope and magnetic field data and sends it to the server open by evhttp.

evhttp saves the latest information about each parameter and informs Lua new data is available using multithreading.

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
