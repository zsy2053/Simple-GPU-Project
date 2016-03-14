Overview:
Simple gpu-accelerated AES encryption program written in C, cuda and OpenCL. We implemented counter mode.
Code was programmed for and tested on NVidia GTX-480 and GTX-780.
This is an old project for ECE1782(Programming Massively Parallel Multiprocessors and Heterogeneous Systems), at the University of Toronto, Fall 2013.



The aes program is used as follows:
./aes -i <input> -k <key> -c <ctr_init> [-o <output>] [-s] [-p] [-m <cpu|cuda|opencl>]
         -i <input>     	input file to encrypt
         -k <key>       	key to use for encryption
         -c <ctr_init>  	initialize counter to value specified in ctr_init file
         -o <output>    	output file (default is <input>.out)
         -s             	input is a ppm file, so do not encrypt/decrypt the header
         -p             	print output (verbose)
         -m             	method (default is cpu)
		 
The minimum input arguments are the input file to be encrypted, the key to use for encryption, and the value used to initialize the counter. 


To check that two binary files are identical run:
diff <(xxd file_one) <(xxd file_two)
If this command yeilds no output, the files are identical.


ORIGINS OF PROJECT NAME:
We used a random word generator found online and chose Wattless from the options that popped up.
