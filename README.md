# Operating System HW2
## Introduction
This is HW2 which inplemented by RaelJung, student no. 21900658.
This program is process that compares the results of two c programming files target.c and solution.c.

The functions used here are as follows:
1. fork()
2. pipe(dup2)
3. poepn()

## fork function
Once fork function run, a new process is created, which call as 'child process'. And it run code independantly without being affected by the parent process. Since we can't control the schedule of executing parent process and child process, we don't know which process will executing first. The scheduler controls the schedule of process run.

## Pipe
Pipe is used to accessing target executing file and to interacting with parent process, since target is executed in child process. Basely, we use pipe variable which is intager type array. And it works as reading file, and writing file. In this program I use 0 to read, 1 to write. Because of this, parent and child process can convey the data of c files result.

## popen()
The popen function is used to get the result of target.c file. It allows program to create an executing file of C file instead of gcc command. So we can see the result of target file. In this program, target file do 5+5. Moreover the result of target.c is printed out in parent process since we use pipe structure.
