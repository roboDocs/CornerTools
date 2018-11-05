Corner Tools
============

This extension is a set of tools to work on corners of an outline. It comprises a tool available in the glyph editing view that allows you to round/cut corners by dragging to define the radius, and a pop-up window (accessible via the Extensions menu, under Corner Tools) which provides a more global set of controls.

## Table of Contents

- [Glyph view rounding tool](#)
    - [Actions](#)
    - [Modifier keys](#)
- [Corner Tools controller](#)
    - [Build](#)
    - [Break](#)
    - [Pit](#)

## Glyph view rounding tool

### Actions

+ **Double-click**: apply rounding
+ **Command+Double-click**: reset all radiuses

### Modifier keys

+ **Shift**: radius steps 5 by 5
+ **Option**: make a flat corner rather than round
+ **Shift**+**Command**: reset radius

![](images/cornerTools-RoundingTool.png)

## Corner Tools controller

The controller works as a wysiwyg corner editor, working with point selection. There are three modes:

### Build

Needs a selection of one or several segments and will try to grow new corners where it can. Results may vary.

![](images/cornerTool-build.png)

### Break

This mode allows similar operations to what the rounding tool but with finer control and the ability to apply the same value to several corners at once. The two parameters allow you to do a number of things:

![](images/cornerTool-break-round.png)
![](images/cornerTool-break-cut.png)
![](images/cornerTool-break-overlap.png)

### Pit

This mode implements ‘ink-traps’ or ’light-wells’ or whatever name fits your ideology. Having no opinion on the matter, I decided to take on another term, pits. Something wicked this way comes.

![](images/cornerTool-pit.png)

(If you get unexpected results, it may be that your contour direction isn’t right. And beyond that, it may well be that you overstep the capabilities of this code: bear in mind that outline modification is a tricky business, so don’t expect miracles.)
