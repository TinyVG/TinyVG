# `.tvg`: Tiny Vector Graphics

A new format for simple vector graphics.

## Why?

Quoting the german Wikipedia on SVG:

> Praktisch alle relevanten Webbrowser können einen Großteil des Sprachumfangs darstellen.

Translated:

> Virtually all relevant web browsers can display most of the language specification.

SVG is a horribly complex format, allowing the embedding of JavaScript and other features no sane person ever wants to have in their images. Other relevant vector graphics formats do not exit or don't have a documentation or specification (looking at you, [HVIF](https://en.wikipedia.org/wiki/Haiku_Vector_Icon_Format)!).

This project tries to create and specify a new vector format suitable for:
- Small and medium icons (think toolbar, buttons, …)
- Low complexity graphics (think graphs, diagrams, …)
- Embedded platforms (low resource requirements)

## Project Goals

Create a vector graphics format that fulfils the following requirements:
- Binary encoded
- Small file size (must be smaller than equivalent bitmaps or SVG graphics)
- Can be rendered without floating point support (suitable for embedded)
- Can be rendered efficiently with modern GPUs (suitable for PC, games)
- Supports the following drawing primitives:
  - points / circles
  - lines
  - triangles / polygons
- Support drawing styles
  - filled
  - outline
  - filled with outline
- Support
  - flat colors
  - bitmap textures
  - linear gradients
- Can use hinting to allow really small rendering (16²)

## Project Status

This project is currently work-in-progress and there's neither a specification or a reference implementation. Consider this a mind-experiment for now