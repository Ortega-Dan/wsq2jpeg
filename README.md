wsq2jpeg - A Wavelet Scalar Quantization algorithm (WSQ) conversion library
===========================
Is a library to convert wsq images to jpeg format and vice versa. Allows individual or batch processing. Only supports images in grayscale. 
# Building form sources
## Pre-requisites
### Linux
```sh
 $ [sudo] apt-get install build-essential autoconf libtool pkg-config
```
## Compile NBIS
### Linux

Download official nist "NBIS Software" from: 
https://www.nist.gov/services-resources/software/nist-biometric-image-software-nbis or 
https://www.nist.gov/itl/iad/image-group/products-and-services/image-group-open-source-server-nigos

Have all the files extracted inside the third_party/nbis directory, in the way that the setup.sh is placed in the following relative path:
[thisProjectRoot]/third_party/nbis/setup.sh

then do the following

```sh
 $ cd third_party/nbis
 ./setup.sh . --without-X11 --64
 $ make config && make it
 $ cd ../..
 ```
 
 From there you are able to debug and develop on top of this proyect with a cmake enabled ide, or just compile (and install) if needed with the following instructions:
 
 
 ## Compile and install
 ### Linux
 ```sh
 $ mkdir build 
 $ cd build
 $ cmake .. && make
 $ [sudo] make install
 ```
 ## Run examples
### WSQ to jpeg
```sh
 $ ./test_wsq ../test ../test 80
 ```
 ### jpeg to wsq 5:1
```sh
 $ ./test_jepg ../test ../test 2.25 
 ```
 
 ### jpeg to wsq 15:1
```sh
 $ ./test_jepg ../test ../test 0.75
 ```
