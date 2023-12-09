# gmake_hw
Linux GNU Make homework

## Usage

### Getting started

1) Clone the repository.
    ```git clone https://github.com/yur4sh/gmake_hw.git```
2) Go to repo directory.
    ```cd gmake_hw```

### Task #1

1) Go to the task #1 directory:
    ```cd make_task1```  

2) To build the project (substitute 'X' with makefile number):
    ```make -f Makefile_X```

3) Test if task_1 project is successfully built:
    ```./task_1```

4) To clean local build artifacts (substitute 'X' with makefile number):
    ```make -f Makefile_X clean```

### Task #2

1) Go to the task #2 directory:
    ```cd make_task2```  

2) To build the project (substitute 'X' with method number).
   Method '1' is 'make -f', '2' stands for 'include .mk':
    ```make METHOD=X```

3) Test if task_2 project is successfully built:
    ```./task_2```

4) To clean local build artifacts.
   Added clean to .PHONY target to ignor empty 'clean' file:
    ```make clean```
