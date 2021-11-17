# Lua Portfolio
*See also: **[C++ Portfolio](cpp-portfolio.md)***.

---

Started learning in 2017.

Teaching and helping, code-reviewing since 2018. Read "Programming In Lua" book (made by Lua authors).

Developing my own Lua course that covers everything from basic things up to Lua C API. (can be shown on a request).

Developing [my own Lua-derived language](https://github.com/GitSparTV/LLLua) made in LuaJIT that compiles to bytecode.

I worked in Lua 5.1, LuaJIT, Garry's Mod Lua, Love2D, Solar2D (Corona2D), Nelua, Luvit and NodeMCU (eLua).

---

# Contributions

## LuaJIT Benchmarks
### *https://github.com/GitSparTV/LuaJIT-Benchmarks*

Big research on how to optimize your code for LuaJIT and Lua.

Page consists many cases about various functions and compare their speed, instructions count and memory consumption.

Page available at https://gitspartv.github.io/LuaJIT-Benchmarks/.

[3rd edition](https://github.com/GitSparTV/LuaJIT-Benchmarks/tree/3rd_edition) is currently in development.

The 3rd edition will look like this:
<details>
  <summary>Image (click to show)</summary>
  <p>
    <img src="https://github.com/GitSparTV/LuaJIT-Benchmarks/raw/3rd_edition/3rd_edition_demo.png">
  </p>
</details>

## Lua Patterns
### *https://github.com/GitSparTV/lua-patterns*

Site for analyzing and learning Lua pattern matching syntax.
Written in JS, pattern matching lexer was taken from Lua source code.

Currently shows explanation of the pattern, has hints, warnings and reports errors. Planned to add more features.

## Lua Infographics
### *https://github.com/GitSparTV/lua-infographics*

Collection of infographics and data about Lua.

For example [top 25 popular .lua file names](https://github.com/GitSparTV/lua-infographics/blob/main/lua-code/lua-code.md#top-25-filenames), [the activity of Lua authors of lua-l mailing list](https://github.com/GitSparTV/lua-infographics/blob/main/lua-popularity/lua-popularity-activity.md#total-emails), [how do people spell Lua? Lua vs LUA](https://github.com/GitSparTV/lua-infographics/blob/main/lua-popularity/lua-popularity-activity.md#lua-word-spelling) 

---

# Lua C API

## lmemprof
### *https://github.com/GitSparTV/lmemprof*

Lua and LuaJIT library to profile memory consumption written in C++.

Currenly just hooks into allocator using lua_setallocf.

New concept will dump what structure exactly are sitting in the memory (like tables, strings, etc).

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

App with Lua runtime with preloaded module for communicating with iCUE SDK (Corsair mices and keyboards).

---

# Code

## LLLua
### *https://github.com/GitSparTV/LLLua*

New language based on Lua, written in Lua and run on LuaJIT.

The idea of the language is to bring static typing, templates, AOT compilation and evaluation, macros and metaprogramming. As the end result you get precompiled Lua chunk.

<details>
  <summary>Example:</summary>
  <p>
    
```lua
-- Can compile a separate function for external linking, but in the code just inlines into `instance.size_`.
-- Or even make everything offset-like and inline to `instance[0]` if `size_` member is the first in the definition.
function class:size() <inline>
    return self.size_
end

-- Internal Lua functions are like C++ constexpr and can evaluate the value at compile-time.
-- Bytecode will have one instruction that pushes literal string "aaaaaaaaaa" onto the stack, string.rep function won't be called.  
print(string.rep("a", 10))
```
    
  </p>
</details>

It originally was planned to make ASM-like language but for Lua that compiles to bytecode: [Version 0.1](https://github.com/GitSparTV/LLLua/tree/v0.1/0.1).

Later on a pack of ideas was combined into [concept 1.0](https://github.com/GitSparTV/LLLua/blob/v0.1/CONCEPT.md).

## Libraries for Garry's Mod
### *https://github.com/GitSparTV/GmodLibraries*

Libraries for Garry's Mod I made while being an owner of a playable server.
Contains network wrappers, text formatting and manipulating functions (supports unicode), json-based database library, user profile library and more.

## Love2D Framework
### *https://github.com/GitSparTV/Files/tree/master/Love2D/Framework*

Love2D framework based on Garry's Mod API for image, GUI, I/O and thread stuff.

<details>
  <summary>Image (click to show)</summary>
  <p>
    <img src="https://user-images.githubusercontent.com/5685050/140625867-90549370-4580-4a70-8a8c-040ef5d810fa.gif" width="50%" height="50%">
  </p>
</details>

## Advent Of Code 2020
### *https://github.com/GitSparTV/Files/tree/master/aoc2020*

My solutions to [Advent Of Code 2020](https://adventofcode.com/2020) -- coding event with daily challenges with text-based algorithms.

## Codewars

I complete challenges on Codewars in Lua.

[See my solutions](https://www.codewars.com/users/GitSparTV/)

<img src="https://www.codewars.com/users/GitSparTV/badges/small">

## University bot
### *https://github.com/GitSparTV/Files/tree/master/UniBot*

Bot, written in Lua, run in Garry's Mod, uses VK API that was helping me in university.

It reports the end of the lesson, tells where the next lesson is, who is the speaker. The schedule is all set from the bot chat.

<details>
  <summary>Image (click to show)</summary>
  <p>
    <img src="https://user-images.githubusercontent.com/5685050/140619152-67ed5d3a-3e03-4db5-96f1-f7e2172ae978.png" width="50%" height="50%">
  </p>
</details>

## Unversity admission advisor

Before university bot I made a bot (with the same configuration) that was fetching admission lists from universities, parsing them, finding people across lists and calculating my chance to get passed for that speciality.

<details>
  <summary>Image (click to show)</summary>
  <p>
    <img src="https://user-images.githubusercontent.com/5685050/141104917-939deab4-cdf4-4fc8-87a6-38cfe912357f.png" width="50%" height="50%">
  </p>
</details>

## C++ iterators
### `https://gist.github.com/GitSparTV/474f71bc18b50e97664cc6db2d033cc8`

C++ iterators implementation in Lua.

## Discord bot libraries
### *https://github.com/GitSparTV/gg.gmod-bot-public*

Libraries of "Toolgun" bot that moderates official Garry's Mod Discord server. (Full code can be requested)

Bot contains, reaction-based dialogs, MDMP parser and analyzer, command handler, spam filter and more.

Written with discordia library using Luvit framework.

## Discord's slash commands support for Discordia
### *https://github.com/GitSparTV/discordia-slash*

Slash commands library for Discord library discordia.

## Series of Garry's Mod addons: GodSentTools
### *https://github.com/GitSparTV/GodSentTools*

A series of addons that helps art and video makers to do job easier and faster.

One of the biggest tool is LocRotScale -- tool to manipulate in-game objects like in Blender.

https://user-images.githubusercontent.com/5685050/142083569-4f881a0a-9703-4bc1-bc21-5b7c304172cc.mp4

https://user-images.githubusercontent.com/5685050/142083733-a78a7e77-f0ec-4e12-93f8-d83f08a84988.mp4

## Garry's Mod addon: EMod
### *https://github.com/GitSparTV/EMod*

Addon for Garry's Mod about electricity.

https://user-images.githubusercontent.com/5685050/142084773-f41abf5a-2f47-4871-a51f-e8c7ca92c2bd.mp4

## Garry's mod addon: gm_sales
### *https://github.com/GitSparTV/gm_sales*

Gamemode for Garry's Mod I was developing for GModStore Gamemode Competition.

## Langston's Ant art generator
### *https://github.com/GitSparTV/Files/tree/master/Love2D/Framework*

Langston's Ant implementation in Love2D that generates art.

https://user-images.githubusercontent.com/5685050/140621217-24c9c659-4c8a-4065-8c3d-3cd6d09780d6.mp4

## Bruteforcer for the level from School 21
### *https://github.com/GitSparTV/Files/tree/master/Love2D/School21*

To get into [School 21 by Sberbank](https://21-school.ru/) you need to complete tasks and levels.

I stuck on some level and decided to bruteforce it to see if it was even possible

<details>
  <summary>Image (click to show)</summary>
    <img src="https://user-images.githubusercontent.com/5685050/140622968-660e1c29-db43-430e-b17a-6fbdf7f0e11f.gif" width="50%" height="50%">
</details>

## Optimization of Garry's Mod addon
### *https://github.com/GitSparTV/cavefight*

Fork of a Garry's Mod addon.

Using my fork the addon increased speed in about 20% and stopped freezing by huge amounts of computations.

## Program for making Garry's Mod addons easier
### *https://github.com/GitSparTV/AddonForge_obsolete*

App made with LuaPower framework collection to create Garry's Mod addons using program with simple UI. 

[![HitCount](http://hits.dwyl.com/GitSparTV/lua-portfolio.svg?style=flat)](http://hits.dwyl.com/GitSparTV/lua-portfolio)
