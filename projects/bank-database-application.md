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

  <img width="800px" class="img-fluid" src="../img/BankDatabase1.png">

This Bank Database Application is a solo project I completed in my Program Structure course (ICS 212) at the University of Hawaiʻi at Mānoa. I designed and implemented a user-friendly interface and database functions, allowing users to add, search, delete, and view customer records. I developed the application in both C and C++ using the UNIX operating system.

To efficiently manage the build process, I created a Makefile to handle the creation and updating of object files and the executable, including the option to run the program with or without debug mode through specified rules. I initially programmed the project in C and then ported it to C++. For the C project, I created header files containing the data structure for records and the function prototypes for the database functions. For the C++ project, I created header files containing the data structure for records and the class definition for managing records. The source files are separately organized for the user interface and database functions.

I learned how to approach various challenges I encountered while coding in C, including ensuring that no memory allocated on the heap was lost, inserting a new node into a linked list without disrupting the rest of the list, and effectively using pointers in a larger project with over a thousand lines of code. While translating the project from C to C++, I learned how to accomplish the same tasks in C++ and gained experience with implementing a copy constructor, overloading the assignment operator (operator=), and overloading the stream insertion operator (operator<<).

Here is a portion of the code for the add function of the Bank Database Application in C:

```cpp
int addRecord(struct record ** startAddress, int uaccountno, char uname[], char uaddress[])
{
    int stop;
    int result;
    struct record * new;
    struct record * addressOfPrevious;
    struct record * addressOfNext;

    stop = 0;
    result = -1;

    if (debugmode == 1)
    {
        printf("\nDebug Message:\n");
        printf("The addRecord function has been called.\n");
        printf("The function parameter names and values are listed below,\n");
        printf("uaccountno: \n%d\n", uaccountno);
        printf("uname: \n%s\n", uname);
        printf("uaddress: \n%s\n", uaddress);
    }

    if (*startAddress == NULL)
    {
        *startAddress = (struct record *)malloc(sizeof(struct record));
        (*startAddress) -> accountno = uaccountno;
        strcpy((*startAddress) -> name, uname);
        strcpy((*startAddress) -> address, uaddress);
        (*startAddress) -> next = NULL;

        result = 0;
    }
```

The printall function displays all customer records in the database.

  <img width="800px" class="img-fluid" src="../img/BankDatabase3.png">

The find function retrieves the customer record for the given account number, and the delete function removes the customer record associated with the provided account number.

  <img width="800px" class="img-fluid" src="../img/BankDatabase4.png">

The image below shows that the customer record was deleted.

  <img width="800px" class="img-fluid" src="../img/BankDatabase5.png">

The quit function allows the user to exit the program.

  <img width="800px" class="img-fluid" src="../img/BankDatabase6.png">

To see the code for my Bank Database Application in C, click <a href="https://github.com/jaylin-m/ICS-212/blob/main/project1.tar.gz">here</a>. To see the code for my Bank Database Application in C++, click <a href="https://github.com/jaylin-m/ICS-212/blob/main/project2.tar.gz">here</a>.
