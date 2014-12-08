Some of problems I ran into: when I move for-loop into thread function, some 
variables declared in the main function are not recognized.
I forget to put scaled color back to package structure sent to thread function.
I did not allocate for loop for different threads according to their thread
ID, causing the function to take the same amount of time regardless of how
many threads are used.
Compiler did not recognize the thread create and thread join function.
Memory leak due to forgeting to free thread structure, which is an array of pthread_t pointers.

When operating under 8 threads, the program speed up to 4 times than the 1 thread implemetation.
