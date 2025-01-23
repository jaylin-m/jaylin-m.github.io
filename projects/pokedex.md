---
layout: project
type: project
image: img/Pokedex.jpg
title: "Pokédex"
date: 2023
published: true
labels:
  - C++
  - UNIX
  - Makefile
summary: "I developed a Pokedex program in C++ that uses each Pokémon's nickname as a key to access and display their information: name, type, and weight."
---

<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>

This Pokédex program is a solo project I completed in my Program Structure course (ICS 212) at the University of Hawaiʻi at Mānoa.


For this project, I was the lead programmer who was responsible for programming the various capabilities of the mouse.  I started by programming the basics, such as sensor polling and motor actuation using interrupts.  From there, I then programmed the basic PD controls for the motors of the mouse.  The PD control the drive so that the mouse would stay centered while traversing the maze and keep the mouse driving straight.  I also programmed basic algorithms used to solve the maze such as a right wall hugger and a left wall hugger algorithm.  From there I worked on a flood-fill algorithm to help the mouse track where it is in the maze, and to map the route it takes.  We finished with the fastest mouse who finished the maze within our college.

Here is some code that illustrates how we read values from the line sensors:

```cpp
byte ADCRead(byte ch)
{
    word value;
    ADC1SC1 = ch;
    while (ADC1SC1_COCO != 1)
    {   // wait until ADC conversion is completed   
    }
    return ADC1RL;  // lower 8-bit value out of 10-bit data from the ADC
}
```

To see the code for my Pokédex program, click <a href="https://github.com/jaylin-m/ICS-212/blob/main/homework9.tar.gz">here</a>.
