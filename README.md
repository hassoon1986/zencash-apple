

### Build instructions
```shell
# run once to install Xcode CLI tools
$ xcode-select --install
# clone and build Horizen
$ git clone https://github.com/HorizenOfficial/zencash-apple.git
$ cd zencash-apple
$ source environment
$ make
```

In case of an error please run the following command for debug info
```shell
$ PRINT_DEBUG=y make all
```
Clone the Horizen repository and fetch the necessary parameters:
Build using the following command (with NUM_CORES = number of cores to use for the build process):

```shell
git clone https://github.com/HorizenOfficial/zen.git
cd zen/
./zcutil/fetch-params.sh
LIBTOOLIZE=glibtoolize ./zcutil/build-mac-clang.sh --disable-libs -j(NUM_CORES)
```

for example:

```shell
LIBTOOLIZE=glibtoolize ./zcutil/build-mac-clang.sh --disable-libs -j4
```
or
```shell
export LIBTOOLIZE=glibtoolize
 ./zcutil/build-mac-clang.sh --disable-libs -j4
 ```
 ### Build with the tools already compiled (example having all the sources in the ~/sources/ folder)
```shell
$ cd ~/zencash-apple
$ source environment
$ cd ~/zen
$ export LIBTOOLIZE=glibtoolize
$ ./zcutil/build-mac-clang.sh --disable-libs -j4 
```
 
 
### Disclaimer
this is a fork of https://github.com/kozyilmaz/zcash-apple.git

