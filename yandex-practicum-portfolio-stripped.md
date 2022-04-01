# Yandex.Practicum.CPP
Portfolio of finished projects during Yandex.Practicum "C++ Developer" course.

[C++ Developer course](https://practicum.yandex.ru/cpp/) is based on C++17 standard.

In this course I learned main STL/STD containers, iterators, algorithms, lambda functions (including IILE), templates, template classes, forwarding reference, rvalue reference and move semantics, copy-and-swap semantics.

Unit-testing, TDD, exceptions, sanitizers, gdb debugging, profiling, coding with code style, making right decision for choosing arguments and returned value.

Operator overloading, threads, async, mutexes, parallel algorithms, rating algorithms by Big O notation, polymorphism, inheritance (including virtual and private), RAII, io and file streams, smart pointers and more.

## [Transport Catalogue](https://github.com/GitSparTV/Yandex.Practicum.CPP/tree/master/TransportCatalogue)

Catalogue of transport routes. I/O is done with JSON, map with routes is rendered using self-made SVG library.

<details>
<summary>Input JSON:</summary>
<p>

```json
{
  "base_requests":[
    {
      "type":"Bus",
      "name":"Route 2",
      "stops":[
        "Station 1",
        "Station 2",
        "Station 3",
        "Station 1"
      ],
      "is_roundtrip":true
    },
    {
      "type":"Bus",
      "name":"Route 1",
      "stops":[
        "Station 4",
        "Station 5"
      ],
      "is_roundtrip":false
    },
    {
      "type":"Stop",
      "name":"Station 5",
      "latitude":43.587795,
      "longitude":39.716901,
      "road_distances":{
        "Station 4":850
      }
    },
    {
      "type":"Stop",
      "name":"Station 4",
      "latitude":43.581969,
      "longitude":39.719848,
      "road_distances":{
        "Station 5":850
      }
    },
    {
      "type":"Stop",
      "name":"Station 2",
      "latitude":43.598701,
      "longitude":39.730623,
      "road_distances":{
        "Station 3":3000,
        "Station 1":4300
      }
    },
    {
      "type":"Stop",
      "name":"Station 3",
      "latitude":43.585586,
      "longitude":39.733879,
      "road_distances":{
        "Station 1":2000,
        "Station 2":3000
      }
    },
    {
      "type":"Stop",
      "name":"Station 1",
      "latitude":43.590317,
      "longitude":39.746833,
      "road_distances":{
        "Station 2":4300,
        "Station 3":2000
      }
    }
  ],
  "render_settings":{
    "width":600,
    "height":400,
    "padding":50,
    "stop_radius":5,
    "line_width":14,
    "bus_label_font_size":20,
    "bus_label_offset":[
      7,
      15
    ],
    "stop_label_font_size":20,
    "stop_label_offset":[
      7,
      -3
    ],
    "underlayer_color":[
      255,
      255,
      255,
      0.85
    ],
    "underlayer_width":3,
    "color_palette":[
      "green",
      [
        255,
        160,
        0
      ],
      "red"
    ]
  },
  "stat_requests":[
    {
      "id":1218663236,
      "type":"Map"
    }
  ]
}
```
</p>
</details>

SVG Result:
![SVG Result](TransportCatalogue/svg.png)

## [Search Server](https://github.com/GitSparTV/Yandex.Practicum.CPP/tree/master/SearchServer)

A search system with plus, minus and stop words support, pagination and unit-tests.

Made with concurrent map, multithreading, iterators and exceptions.

SearchServer class is initialized with stop words. Documents are added using `AddDocument` method. Method supports different type of documents: actual, removed, irrelevant and banned.

## [Recreating VFTable](https://github.com/GitSparTV/Yandex.Practicum.CPP/tree/master/VFTableRecreation)

There was a company `PII` - Polymorphism, Incapsulation and Inheritance.

One co-owner left and took inheritance. Now it's `PI`. 

The task is to recreate inheritance and their virtual methods without using C++ inheritance. 

## [Selfmade STL](https://github.com/GitSparTV/Yandex.Practicum.CPP/tree/master/SelfmadeSTL)
Learning C++17 with remaking STL containers and utilities such as: vector (including simple and full version), optional, single linked list and unique_ptr analogue.

Uses unit-testing, perfect forwarding, rvalue reference overloading, variadic templates, iterators, placement new, copy-and-swap semantic, move semantic and more.

## Peer-review projects

These projects were part of a peer-review: students review the work of each other.

### [EBook](https://github.com/GitSparTV/Yandex.Practicum.CPP/blob/master/ebook.cpp)
Program that tracks people progress on 1 book.

`Cheer` command tell the person how many people have read it more than him.

### [Restricted Domains](https://github.com/GitSparTV/Yandex.Practicum.CPP/blob/master/domains.cpp)

Program that checks if the domain is restricted

Input:
```
4
gdz.ru
maps.me
m.gdz.ru
com
7
gdz.ru
gdz.com
m.maps.me
alg.m.gdz.ru
maps.com
maps.ru
gdz.ua
```

Output:
```
Bad
Bad
Bad
Bad
Bad
Good
Good
```
