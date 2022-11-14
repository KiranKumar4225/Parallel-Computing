# AES ENCRYPTION PASSWORD CRACKING THROUGH PARALLELISATION

Module: Parallel Computing 
Module code: UFCFFL-15-M
Submitted by: Kiran Kumar Mohanraj

## Coursework Outline

The aim is to implement parallel algorithms using OpenMP and OpenMPI from the serial program provided. The performance of the parallel algorithm should be analysed against the sequential performance.

### Runtime
* ##### OpenMP:

    1. Download the crackaesmp.c file to the desired directory.
    2. To compile the file, type "gcc -o out.o crackaesmp.c -fopenmp -lcrypto".
    3. Once the compilation is done, To run the program, type "./out.o".
    4. The results will be in this format : "Password is xxxxx Time elapsed is xx seconds".
To run the code with different thread change the variable num_thrd in the code.

* ##### OpenMPI:

    1. Download the crackaesmpi.c file to the desired directory.
    2. To compile the file, type "mpicc -o out crackaesmpi.c -lcrypto"
    3. To run the program, type "mpirun -np x out", where x is the number of processors. To run the program with different processes, change the value of x.
    4. The results will be in this format : "Password is xxxxx Time elapsed is xx seconds".

For running the code with backward and forward dictionary, just uncomment the desired dictionary and run the program.

#### Benchmarking Tests
For analysing the performance of the parallel implementation, 5-length password is used, which is "Mar10". The dictionary with Frequency distribution of English letters is used. 
Forward dictionary – 
"ETANOISHRDLUCMWFYGPBVKXJQZetanoishrdlucmwfygpbvkxjqz0123456789"
Backward dictionary –
"9876543210zqjxkvbpgyfwmculdrhsionateZQJXKVBPGYFWMCULDRHSIONATE"

The results for the performance analysis are provided in the logbook.