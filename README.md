# JEngine

## Contents

- Description
- Stuff you should probably know
- Installation
- Prefrences
	- Versions
	- Cursor
	- Audio
	- Code organization
	- Input detection
- Functions and their usage
	- Non-JEngine Functions
	- Button Functions
	- Utility Functions
	- Image Functions
	- Setup Functions
	- Keypress Functions

## Description

JEngine is a Javascript canvas game template that comes packaged in one HTML file with a few template graphics. JEngine is completely free to use in any projects with no credit whatsoever. I just want to help people.

## Stuff you should probably know

- JEngine was made by me, a random 15 year old on the internet, so it is not expertly made at all, but it may just fit your niche needs.
- The J in JEngine does not come from Javascript, it is completely unrelated to the J in Javascript. If JEngine was named after Javascript it would be called JSEngine, which it is *not* called.
- This is the very first thing I've ever put onto Github so please be nice if I mess up one of the traditional ways of doing stuff here.

## Installation

Installation is really easy. Download either the empty version or the bloated version of JEngine, and you're already all set.

## Prefrences

### Versions
There are two versions of JEngine you can get: An empty version, and a bloated version. The empty version has only JEngine in it, and no other setup code. The bloated version starts with all setup functions and frame functions.

### Cursor

By default, JEngine uses a custom cursor. The cursor interracts with buttons by changing color when hovering over a button.

### Audio

By default, JEngine comes with an \<audio\> element. This is just to save you the hassle of putting one in, but if you prefer to use a different way of playing audio, be my guest.

### Code Organization

By default, JEngine comes with different sections to organize code. Keeping this is up to you, since it will only affect your workflow.

### Input Detection

By default, bloated JEngine comes with keypress functions and a wasd controller. These can be removed if you want to use a different method of input detection. The empty version of JEngine does not include input detection.

## Functions and their usage

### Non-JEngine Functions

#### SETUPALL()

A function only run once, which, as the name suggests, sets up all the variables.

#### updateAllStuff()

A function that updates every animationframe.
By default, JEngine does not directly run scripts inside updateAllStuff(), instead opting to 

#### updateVariables()

By default inside of the updateAllStuff() function. It is a function that you do not necessarily need to have, but I find it useful to separate graphical updates from variable updates.

#### updateCanvas()

By default inside of the updateAllStuff() function. Once again, it is a function that you do not necessarily need to have, but I find it useful to separate graphical updates from variable updates.

#### mouseClick()

Run every time the mouse clicks. via the canvas's onclick="mouseClick".

#### coordinate(event)

coordinate() is run when the mouse's position changes on the canvas. By default, it only calculates the mouse's X and Y position on the canvas relative to its position and size.

#### drawButton(i)

Used for debugging purposes, and can be removed immediately if needed.

### Button Functions

#### JEng.addButtonListener(name, setcursor, x, y, width, height)

Adds each provided element into an object and adds that object to BUTTONLIST.

#### JEng.checkButtonList()

Checks if the cursor is touching any buttons, and if it is, changes the cursor.

### Utility Functions

#### JEng.getScreenFactor()

Returns target width/window width.

#### JEng.calcFPS

Calculates the FPS after every second.

#### JEng.drawOutline(i)

Seems to be broken, i'll probably remove it eventually.

#### JEng.drawLine(a, b, c, d)

Draws a line between two 2D points.

### Image Functions

#### JEng.img(img)

Checks the imageCache for an image with the provided name, and returns an image.

#### JEng.rotateAndDrawImage(image, degrees, x, y)

Rotates an image and draws it centered.
I did not write this specific function, I got microsoft copilot to generate it for me.

#### JEng.drawCenteredParalaxImage(img, xoffset, yoffset, xsize, ysize, Xparalax, Yparalax)

Draws a centered image and changes the position to follow the mouse cursor by some value. Keep in mind that xsize and ysize are not pixel values, but are used to multiply by the image's size.

#### JEng.drawCenteredImage(imgName, xoffset, yoffset, xsize, ysize)

Draws a centered image. Keep in mind that xsize and ysize are not pixel values, but are used to multiply by the image's size.

### Setup Functions

#### JEng.SETUPZOOM()

calculates the size of the canvas and zooms the canvas appropriately. This function is run more than once, even though it is a setup function.

#### JEng.SETUPIMAGES()

adds every image from the imageURLs array to the imageCache array.

### Keypress Functions

#### JEng.isKeyPressed(key)

Returns weather or not if the specified key is pressed.
