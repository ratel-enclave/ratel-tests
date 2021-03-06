[Iozone Benchmark](http://www.iozone.org/)
=======================

Building Iozone for Ratel
-----------------------------

### Building Iozone from Source:

Use the following command(s) to download the latest source code of iozone:
  ```
    $ git clone https://github.com/ratel-enclave/ratel-tests.git .
  ```
Go to the target directory:
  ```
    $ cd iozone-3.487/src/current
  ```
We have already added -pie -fPIC option in the Makefile. So you need to run **make** with the architecture type of your system (which should be AMD64 to support Ratel).
  ```
    $ make linux-AMD64
  ```
How to Run Iozone with Ratel?
-----------------------------------
Just like other applications run with the specified parameters:
  ```
    $ ./ratel -- ./iozone -a -q 4096
  ```
For more iozone running options you can take a look at [here](http://www.iozone.org/docs/IOzone_msword_98.pdf).

**NOTE**: Currently Ratel supports upto 4096 KB of record size without any bugs. For other parameters any value can be chosen.
