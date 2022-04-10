# Drawing a heart in Python 

Hi fellow coders!

This project was created to have some fun with Python during my Sundays. In this project I drawn a heart in Python using `turtle` framework. 

Before to dive into the description of the project I'll leave here a brief description about `turtle` framework. If you're not interested about it or you have some experience with this framework you can jump to the [Project Overview](#project-overview) section. Thanks 🙌


# Table of contents 
1. [Turtle Graphics](#turtle-graphics)
    - [Framework Overview](#framework-overview)
    - [Drawing using Turtle](#drawing-using-turtle)
2. [Project Overview](#project-overview)
    - [The code inside the project](#the-code-inside-the-project)
4. [References](#references)


# Turtle Graphics

Accordingly to Python's documentation : 

> Turtle graphics is a popular way for introducing programming to kids. It was part of the original Logo programming language developed by Wally Feurzeig, Seymour Papert and Cynthia Solomon in 1967.

Indeed, thanks to Turtle Graphics and obviously to Turtle module, programmers can create beautiful shapes ny simply using its methods. It's a very fascinating way to approach to Python and to computer programming in general. 

Imagine a robotic turtle starting at (0, 0) in the x-y plane. After an import turtle, give it the command turtle.forward(15), and it moves (on-screen!) 15 pixels in the direction it is facing, drawing a line as it moves. Give it the command turtle.right(25), and it rotates in-place 25 degrees clockwise.

By combining together these and similar commands, intricate shapes and pictures can easily be drawn.

**The turtle module is an extended reimplementation of the same-named module from the Python standard distribution up to version Python 2.5. It tries to keep the merits of the old turtle module and to be (nearly) 100% compatible with it.**

## Framework Overview

The turtle module provides turtle graphics primitives, in both object-oriented and procedure-oriented ways. Because it uses tkinter for the underlying graphics, it needs a version of Python installed with Tk support.

The object-oriented interface uses essentially two+two classes:

1. The TurtleScreen class defines graphics windows as a playground for the drawing turtles. Its constructor needs a tkinter.Canvas or a ScrolledCanvas as argument. It should be used when turtle is used as part of some application. The function Screen() returns a singleton object of a TurtleScreen subclass. This function should be used when turtle is used as a standalone tool for doing graphics. As a singleton object, inheriting from its class is not possible. All methods of TurtleScreen/Screen also exist as functions, i.e. as part of the procedure-oriented interface.
2. RawTurtle (alias: RawPen) defines Turtle objects which draw on a TurtleScreen. Its constructor needs a Canvas, ScrolledCanvas or TurtleScreen as argument, so the RawTurtle objects know where to draw. Derived from RawTurtle is the subclass Turtle (alias: Pen), which draws on “the” Screen instance which is automatically created, if not already present. All methods of RawTurtle/Turtle also exist as functions, i.e. part of the procedure-oriented interface.

The procedural interface provides functions which are derived from the methods of the classes Screen and Turtle. They have the same names as the corresponding methods. A screen object is automatically created whenever a function derived from a Screen method is called. An (unnamed) turtle object is automatically created whenever any of the functions derived from a Turtle method is called.

**To use multiple turtles on a screen one has to use the object-oriented interface.**

## Drawing using Turtle

To make use of the turtle methods and functionalities, we need to import turtle.**”turtle” comes packed with the standard Python package and need not be installed externally**. The roadmap for executing a turtle program follows 4 steps:  

1. Import the turtle module
2. Create a turtle to control.
3. Draw around using the turtle methods.
4. Run turtle.done().

So as stated above, before we can use turtle, we need to import it. We import it as : 
```python
from turtle import *
# or
import turtle
```

After importing the turtle library and making all the turtle functionalities available to us, we need to create a new drawing board (window) and a turtle. Let’s call the window as `window` and the turtle as `my_turtle` (because we have a lot of fantasy). So we code as: 

```python
window = turtle.Screen()
window.bgcolor("black") #you can choose the color you prefer
window.title("Turtle")
my_turtle = turtle.Turtle()
```

Now that we have created the window and the turtle, we need to move the turtle. To move forward 100 pixels in the direction `my_turtle` is facing, we code: 

```python
skk.forward(100)
```

We have moved `my_turtle` 100 pixels forward, Awesome! Now we complete the program with the `done()` function and We’re done! 

```python
turtle.done()
```

So, we have created a program that draws a line 100 pixels long. We can draw various shapes and fill different colors using turtle methods. There’s plethora of functions and programs to be coded using the turtle library in python.

# Project Overview
The project is very easy and very fun to do on your own. It allows you to use a lot of methods from **Turtle framwork**. There is just one functions that I wrote to effectivly draw the heart on the screen. For the rest, they are all within the framework. 

In pratice: the project draw a heart on a black screen and coloring in pink the heart itself. 

The reasoning behind the project is very basic. Since the heart is a *simmetric shape* I've decided to split the code in two parts each one divided by the `draw()` function. In this way I can do the same exact thing, that I've done on the left, on the right.  

## The code inside the project 
After importing the `turtle` framework

```python
import turtle
#or
from turtle import * #it's the same thing of the code above
```
I've started to give some informations about the speed of drawing, the background color and the size of the mark on the board
```python
turtle.speed(3)
turtle.bgcolor('black') #I've set a black board to show up better the heart color
turtle.pensize(3)
```
Then I created my loop to give instructions to the turtle pen about where to go and embedded all in function called `draw()`
```python
def draw():
    for i in range(200):
        turtle.right(1)
        turtle.forward(1)
```
In the end I set the color of the pen and the color of the shape
```python
turtle.color('red', 'pink') #you can choose whetever color you prefer
```
After all of this I've just put together all the turtle's methods that suited best for my homework
```python
turtle.begin_fill()
turtle.left(140)
turtle.forward(111.65)
draw() #This is the function that I've created
turtle.left(120)
draw() 
turtle.forward(111.65)
turtle.end_fill()
turtle.hideturtle()
turtle.done()
```
**Note**: As you can notice the `draw()` function is written two times, this because the heart that I drawn is a symmetric shape and you can do the same thing on both side, the left side and the right side. 

Thanks for reading. 🥳🥳🥳

*If you want to follow me on my other socials I'll appreciate it.*
- *[Medium](https://medium.com/@girolamopinto1)*
- *[Linkedin](https://www.linkedin.com/in/girolamo-pinto-250b89164/)*
- *[Instagram](https://www.instagram.com/girolamopinto/)*
- *[Facebook](https://www.facebook.com/girolamo.pinto)*

# References
- [Python documentation](https://docs.python.org/3/library/turtle.html)
- [GeeksForGeeks](https://www.geeksforgeeks.org/turtle-programming-python/)
