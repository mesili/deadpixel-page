# Dead pixel page

Demo : https://deadpixel.mesili.fr

## Why ?

I wanted to use deadpixelbuddy.com but it looks like the website has been suspended by the hosting company... 

So I quickly made this page to check my -worsening- monitor. 
Nobody asked but if you wonder, it has some dead pixels and now a vertical line of dead or at least darker pixels.

Usually I do not share this kind of quick & dirty snippets but I feel like it would be a great base to teach my son a bit about javascript in a few years...

## What ? 

The purpose of this page is to help locate dead pixels on your screen by showing a flat color that you can change by moving the mouse around (or on tap for mobiles).

## How ? 

Nothing fancy : 
1. An HTMl5 page 
1. A `<body>` with an inner `<div id="filler">`
1. An `mousemove`  event listener on `#filler` 
1. The background color is set using `hsl()`

The value of H, S and L are respectively : 
- H : the current horizontal mouse position divided by the #filler.clientWidth then multiplied by 360
- S : Minimum set a 29%, maximum at 100%. Incrementing or decrementing gradually on each mousemove event
- L : the current vertical mouse position divider by the #filler.clientHeight then multiplied by 100
