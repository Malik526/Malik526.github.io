[Back to Portfolio](./)

Project 4 Binary Search Tree
===============

-   **Class: CSCI 315 Data Structures ** 
-   **Grade: A**
-   **Language(s):Python**
-   **Source Code Repository:** [features/mastering-markdown](https://guides.github.com/features/mastering-markdown/)  
    (Please [email me](mailto:example@csustudent.net?subject=GitHub%20Access) to request access.)

## Project description
Pick two balanced binary search tree implementations (AVL, Red-Black, ScapeGoat, 2-3, AA,
Splay, Treap, etc) and implement my interface.
Next research what situations each perform better or worse in. Namely:
The situation one exhibits better performance. (b) Tell me why you believe that is the case.
Then generate test cases show one performing better than the other. Generate a performance graph.
## How to compiles / run the program

bash
```compile```
AIN=src/main.cpp
SRCS := $(filter-out $(MAIN),$(wildcard src/*.cpp))
CFLAGS=-g -I src/
.PHONY: clean test all
BIN=bt-test

all:
	g++ -o ${BIN} $(CFLAGS) ${SRCS} ${MAIN}

run: all
	./${BIN}

%test:
	cxxtestgen --runner=ErrorPrinter -o tests/test-runner.cpp tests/$@.cpp ${SRCS}
	g++ ${CFLAGS} tests/test-runner.cpp $(SRCS) -o test-runner
	./test-runner

clean:
	rm -rf ${BIN} tests/test-runner.cpp test-runner

Run "make" in terminal while in the correct directrory


## UI Design
This program utilizes creating a search tree in main and running the functions from binarytree.cpp

![screenshot](images/Screenshot_output.png)
Fig 1. The launch screen

![screenshot](images/Screenshot_output.png)