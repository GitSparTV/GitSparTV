# C++ Portfolio
*See also: **[Lua Portfolio](lua-portfolio.md)***.

---

I'm learning C++ in [Yandex.Praktikum](https://practicum.yandex.ru/cpp/) course "C++ Developer" as additional professional education since Feb 2021 (Will graduate in Jan 2022).

I also coded a Linux program, Arduino programs and modules with Lua C API.

# Code

## Yandex.Praktikum
### *https://github.com/GitSparTV/Yandex.Practicum.CPP*

Projects I was making during Yandex.Praktikum "C++ Developer" course.

The course teaches C++ fundamentals and idiomatics, from basic logic up to multithreading, move semantics, remaking STL containers and more.

To see more information, see the repo page.

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

Garry's Mod C++ module written with evhttp (libevent) for Sensor Logger app for iOS.

iOS app reads device accelerometer, gyroscope and magnetic field data and sends it to the server open by evhttp.

evhttp saves the latest information about each parameter and informs Lua new data is available using multithreading.

## LuaWheel
### *https://github.com/GitSparTV/LuaWheel*

Lua module written in C++ with Logitech Wheel SDK.

Allows to get all parameters and fully control Logitech wheel.

<details>
  <summary>Demo in Love2D (click to show)</summary>
  <p>
    <img src="https://github.com/GitSparTV/LuaWheel/raw/master/LuaWheelDemo.gif">
  </p>
</details>

## LuaCUE
### *https://github.com/GitSparTV/LuaCUE*

App with Lua runtime with preloaded module for communicating with iCUE SDK (Corsair mice and keyboards).

[![HitCount](http://hits.dwyl.com/GitSparTV/cpp-portfolio.svg?style=flat)](http://hits.dwyl.com/GitSparTV/cpp-portfolio)