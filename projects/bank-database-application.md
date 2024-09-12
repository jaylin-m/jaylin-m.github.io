---
layout: project
type: project
image: img/Bank.jpg
title: "Bank Database Application"
date: 2023
published: true
labels:
  - C
  - C++
  - UNIX
  - Makefile
summary: "I developed a bank database application that enables users to add, search, delete, and view customer records in both C and C++."
---

<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>

This Bank Database Application is a solo project I completed in my Program Structure course (ICS 212) at the University of Hawaiʻi at Mānoa. I designed and implemented a user-friendly interface and database functions, allowing users to add, search, delete, and view customer records. I developed the application in both C and C++ using the UNIX operating system.

To efficiently manage the build process, I created a Makefile to handle the creation and updating of object files and the executable, including the option to run the program with or without debug mode through specified rules. I initially programmed the project in C and then ported it to C++. For the C project, I created header files containing the data structure for records and the function prototypes for the database functions. For the C++ project, I created header files containing the data structure for records and the class definition for managing records. The source files are separately organized for the user interface and database functions.



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

To see the code for my Bank Database Application in C, click here. To see the code for my Bank Database Application in C++, click here.
