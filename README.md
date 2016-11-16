# libfuzzer-workshop
Materials of *"Modern fuzzing of C/C++ Projects"* workshop.

The workshop will be hosted at [ZeroNights'16] security conference.

## Requirements

* 2-3 hours of your time
* Linux-based OS
* C/C++ experience (nothing special, but you need to be able to read, write and
compile C/C++ code)
* a recent version of clang compiler. Distributions from
package managers are too old and most likely won't work (the workshop
called "modern", right?), you have two options:
	 * checkout **clang** repository and build it yourself. To make it easy, 
	 feel free to use [/checkout_build_install_llvm.sh](checkout_build_install_llvm.sh)
	 script, it has been tested on clean Ubuntu 16.04
	 * a VirtualBox VM with working environment will be provided at the workshop
* `sudo apt-get install -y make autoconf automake libtool`


Fuzzing experience is not required.

## Contents
1. An introduction to fuzz testing
2. An example of traditional fuzzing
3. Coverage-guided fuzzing
4. Writing fuzzers (simple examples)
5. Finding Heartbleed (CVE-2014-0160)
6. Finding c-ares $100,000 bug (CVE-2016-5180)
...

## Prerequisites

### clang

To complete this workshop, you need to use a fresh revision of `clang` and
`llvm-symbolizer` tools. You can use the binaries provided in `bin` directory of
this repository. To use them without specifying an absolute path, you can:
* add `bin` directory to the `PATH` env variable:
```bash
export PATH="$PWD/bin:$PATH"
```
* create symbolic links in `/usr/bin` or any other directory of your choice

### libFuzzer
Building libFuzzer is extreemly easy:
```bash
cd libFuzzer
Fuzzer/build.sh
```


## Links

* libFuzzer documentation: [http://libfuzzer.info](http://libfuzzer.info)
* libFuzzer tutorial: [http://tutorial.libfuzzer.info](http://tutorial.libfuzzer.info)
* Google Online Security Blog: [Guided in-process fuzzing of Chrome components](https://security.googleblog.com/2016/08/guided-in-process-fuzzing-of-chrome.html)


[ZeroNights'16]: https://2016.zeronights.org/program/workshops/#ws1
