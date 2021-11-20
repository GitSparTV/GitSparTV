# Lua Portfolio
*See also: **[C++ Portfolio](cpp-portfolio.md)***.

---

Started learning in 2017.

Teaching and helping, code-reviewing since 2018. Read "Programming In Lua" book (written by Lua authors).

Developing my own Lua course that covers everything from basic things up to Lua C API. (can be shown on a request).

Developing [my own Lua-derived language](https://github.com/GitSparTV/LLLua) made in LuaJIT that compiles to bytecode.

I worked in Lua 5.1, LuaJIT, Garry's Mod Lua, Love2D, Solar2D (Corona2D), Nelua, Luvit and NodeMCU (eLua).

---

# Contributions

## LuaJIT Benchmarks
### *https://github.com/GitSparTV/LuaJIT-Benchmarks*

![7sJAZQJKjS](https://user-images.githubusercontent.com/5685050/142696181-79a8a18c-e53f-441b-b6c1-5b7d0c7cd040.gif)

Big research on how to optimize your code for LuaJIT and Lua.

Page consists many cases about various functions and compare their speed, instructions count and memory consumption.

Page available at https://gitspartv.github.io/LuaJIT-Benchmarks/.

[3rd edition](https://github.com/GitSparTV/LuaJIT-Benchmarks/tree/3rd_edition) is currently in development.

The 3rd edition will look like this:

<img src="https://github.com/GitSparTV/LuaJIT-Benchmarks/raw/3rd_edition/3rd_edition_demo.png" width="50%">

## Lua Patterns
### *https://github.com/GitSparTV/lua-patterns*

![JHECqs5CCn 00_00_00-00_00_30](https://user-images.githubusercontent.com/5685050/142695730-5dadb986-9a5e-4b3d-886f-2fa8bb46ce4b.gif)

Site for analyzing and learning Lua pattern matching syntax.
Written in JS, pattern matching lexer was taken from Lua source code.

[See online](https://gitspartv.github.io/lua-patterns/)

Currently, shows explanation of the pattern, has hints, warnings and reports errors. Planned to add more features.

## Lua Infographics
### *https://github.com/GitSparTV/lua-infographics*

<img src="https://github.com/GitSparTV/lua-infographics/raw/main/lua-popularity/luapopularity_mailinglist.png">

Collection of infographics and data about Lua.

For example [top 25 popular .lua file names](https://github.com/GitSparTV/lua-infographics/blob/main/lua-code/lua-code.md#top-25-filenames), [the activity of Lua authors of lua-l mailing list](https://github.com/GitSparTV/lua-infographics/blob/main/lua-popularity/lua-popularity-activity.md#total-emails), [how do people spell Lua? Lua vs LUA](https://github.com/GitSparTV/lua-infographics/blob/main/lua-popularity/lua-popularity-activity.md#lua-word-spelling) 

---

# Lua C API
## *[See here](cpp-portfolio.md#lua_c_api)*

---

# Code

## LLLua
### *https://github.com/GitSparTV/LLLua*

```lua
-- Example
-- Can compile a separate function for external linking, but in the code just inlines into `instance.size_`.
-- Or even make everything offset-like and inline to `instance[0]` if `size_` member is the first in the definition.
function class:size() <inline>
    return self.size_
end

-- Internal Lua functions are like C++ constexpr and can evaluate the value at compile-time.
-- Bytecode will have one instruction that pushes literal string "aaaaaaaaaa" onto the stack, string.rep function won't be called.  
print(string.rep("a", 10))
```

New language based on Lua, written in Lua and run on LuaJIT.

The idea of the language is to bring static typing, templates, AOT compilation and evaluation, macros and metaprogramming. As the end result, you get a precompiled Lua chunk.

It originally was planned to make ASM-like language but for Lua that compiles to bytecode: [Version 0.1](https://github.com/GitSparTV/LLLua/tree/v0.1/0.1).

Later on, a pack of ideas was combined into [concept 1.0](https://github.com/GitSparTV/LLLua/blob/v0.1/CONCEPT.md).

## Libraries for Garry's Mod
### *https://github.com/GitSparTV/GmodLibraries*

https://user-images.githubusercontent.com/5685050/142705277-2860e4d8-4b57-49ca-8ee6-adc4b2956bc8.mp4

![2018-07-01_22-40-13](https://user-images.githubusercontent.com/5685050/142708507-fb7d8f14-a3f7-452b-b7d4-524c13d5f7b7.gif)

https://user-images.githubusercontent.com/5685050/142708684-8ebfb8fa-428f-4b3a-87dc-af5d683570e9.mp4

![2018-06-29_16-49-40](https://user-images.githubusercontent.com/5685050/142708711-95e3bf56-f9a1-4ddf-bb30-60129557b378.gif)

https://user-images.githubusercontent.com/5685050/142708818-a5e73539-cf58-4610-bbbb-8199f2a50440.mp4

![2018-02-17_20-49-53](https://user-images.githubusercontent.com/5685050/142708866-ad4cae78-b804-478d-b4ed-ff6c51db00a9.gif)

Libraries for Garry's Mod I made while being an owner of a playable server.
Contains network wrappers, text formatting and manipulating functions (supports unicode), json-based database library, user profile library and more.

## Series of Garry's Mod addons: GodSentTools
### *https://github.com/GitSparTV/GodSentTools*

https://user-images.githubusercontent.com/5685050/142083569-4f881a0a-9703-4bc1-bc21-5b7c304172cc.mp4

https://user-images.githubusercontent.com/5685050/142083733-a78a7e77-f0ec-4e12-93f8-d83f08a84988.mp4

A series of addons that helps art and video makers to do job easier and faster.

One of the biggest tools is LocRotScale -- a tool to manipulate in-game objects like in Blender.

## Love2D Framework
### *https://github.com/GitSparTV/Files/tree/master/Love2D/Framework*

<img src="https://user-images.githubusercontent.com/5685050/140625867-90549370-4580-4a70-8a8c-040ef5d810fa.gif" width="50%" height="50%">

Love2D framework based on Garry's Mod API for image, GUI, I/O and thread stuff.

## Discord bot libraries
### *https://github.com/GitSparTV/gg.gmod-bot-public*

https://user-images.githubusercontent.com/5685050/142735572-86d10f4c-d05d-49cf-b6bd-dd79a721b2fe.mp4

<img src="https://user-images.githubusercontent.com/5685050/142735616-1d98744f-19af-48aa-a2e4-94eb92b0ecde.png" width="50%">

Libraries of "Toolgun" bot that moderates official Garry's Mod Discord server. (Full code can be requested)

Bot contains, reaction-based dialogs, MDMP parser and analyzer, command handler, spam filter and more.

Written with discordia library using Luvit framework.

## Advent Of Code 2020
### *https://github.com/GitSparTV/Files/tree/master/aoc2020*

My solutions to [Advent Of Code 2020](https://adventofcode.com/2020) -- coding event with daily challenges with text-based algorithms.

## C++ iterators
### *https://gist.github.com/GitSparTV/474f71bc18b50e97664cc6db2d033cc8*

C++ iterators implementation in Lua.

## MergeSort and BinaryInsertionSort algorithms
### *https://gist.github.com/GitSparTV/0b15a698d4b8b7f8be70e9f262a7468d*
### *https://gist.github.com/GitSparTV/6b5ae920557b7147ae9c29e63d9f3842*

Sorting algorithms rewritten from C++. 

## Discord's slash commands support for Discordia
### *https://github.com/GitSparTV/discordia-slash*

![image](https://user-images.githubusercontent.com/5685050/142735423-5a9064b7-013d-4eef-a874-eec544117dc8.png)

Slash commands library for Discord library discordia.

## Garry's mod addon: gm_sales
### *https://github.com/GitSparTV/gm_sales*

https://user-images.githubusercontent.com/5685050/142698166-4c07bb4e-7b01-4178-9f51-0622916ac847.mp4

https://user-images.githubusercontent.com/5685050/142698258-a1982cee-9f97-4a8f-bfc3-718200b20c3d.mp4

Gamemode for Garry's Mod I was developing for GModStore Gamemode Competition.

## Garry's Mod addon: EMod
### *https://github.com/GitSparTV/EMod*

https://user-images.githubusercontent.com/5685050/142084773-f41abf5a-2f47-4871-a51f-e8c7ca92c2bd.mp4

![hl2_2018-06-25_02-49-02](https://user-images.githubusercontent.com/5685050/142708744-f16378a2-9495-42be-b9cd-ebb151badcb9.png)

Addon for Garry's Mod about electricity.

## Codewars

I complete challenges on Codewars in Lua.

[See my solutions](https://www.codewars.com/users/GitSparTV/)

<img src="https://www.codewars.com/users/GitSparTV/badges/small">

## University bot
### *https://github.com/GitSparTV/Files/tree/master/UniBot*

<img src="https://user-images.githubusercontent.com/5685050/140619152-67ed5d3a-3e03-4db5-96f1-f7e2172ae978.png" width="50%" height="50%">

Bot, written in Lua, run in Garry's Mod, uses VK API that was helping me in university.

It reports the end of the lesson, tells where the next lesson is, who is the speaker. The schedule is all set from the bot chat.

## University admission advisor

<img src="https://user-images.githubusercontent.com/5685050/141104917-939deab4-cdf4-4fc8-87a6-38cfe912357f.png" width="50%" height="50%">

![ShareX_2018-07-27_23-45-03](https://user-images.githubusercontent.com/5685050/142708585-c40b705b-7915-4723-9136-3324f48ddf23.png)

![sublime_text_2018-07-21_14-42-23](https://user-images.githubusercontent.com/5685050/142708609-78ff64a1-88fa-4625-b8c8-aa2b8c710d01.png)

![sublime_text_2018-07-27_23-44-58](https://user-images.githubusercontent.com/5685050/142708626-d5bcd214-9271-4f7f-835f-d2f373a17b9a.png)

Before university bot I made a bot (with the same configuration) that was fetching admission lists from universities, parsing them, finding people across lists and calculating my chance to get passed for that specialty.

## Langston's Ant art generator
### *https://github.com/GitSparTV/Files/tree/master/Love2D/Framework*

https://user-images.githubusercontent.com/5685050/140621217-24c9c659-4c8a-4065-8c3d-3cd6d09780d6.mp4

Langston's Ant implementation in Love2D that generates art.

## Bruteforcer for the level from School 21
### *https://github.com/GitSparTV/Files/tree/master/Love2D/School21*

<img src="https://user-images.githubusercontent.com/5685050/140622968-660e1c29-db43-430e-b17a-6fbdf7f0e11f.gif" width="50%" height="50%">

To get into [School 21 by Sberbank](https://21-school.ru/) you need to complete tasks and levels.

I stuck on some level and decided to bruteforce it to see if it was even possible

## Optimization of Garry's Mod addon
### *https://github.com/GitSparTV/cavefight*

https://user-images.githubusercontent.com/5685050/142703165-4be2b8cb-ba55-4cdb-a353-43ecad7fae0d.mp4

Fork of a Garry's Mod addon.

Using my fork, the addon increased speed in about 20% and stopped freezing by huge amounts of computations.

## Program for making Garry's Mod addons easier
### *https://github.com/GitSparTV/AddonForge_obsolete*

https://user-images.githubusercontent.com/5685050/142700037-28be5b91-f56d-48b8-94ef-960757db2468.mp4

App made with LuaPower framework collection to create Garry's Mod addons using program with simple UI. 

[![HitCount](http://hits.dwyl.com/GitSparTV/lua-portfolio.svg?style=flat)](http://hits.dwyl.com/GitSparTV/lua-portfolio)
