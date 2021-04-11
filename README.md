# lrose-cnvgrb

Copy of NCEP cnvgrb application, adding cmake build wrapper.

## Location of original source

Code copied from:

* [NWS NCEP Codes](https://www.nco.ncep.noaa.gov/pmb/codes/GRIB2/)

## Install required packages

You need to install the following libraries:

* jasper-devel
* libpng-devel
* zlib-devel

## Clone

```
  mkdir -p ~/git
  cd ~/git
  git clone https://github.com/ncar/lrose-cnvgrb
```

### Make build directory and run cmake

```
  cd ~/git/lrose-cnvgrb
  mkdir build
  cd build
  cmake ..
```

### Perform the build

```
  cd ~/git/lrose-cnvgrb/build
  make install
```

### Installation directory

The default install prefix is ```~/lrose```.

The default directories for installation are:

```
  ~/lrose/lib
  ~/lrose/bin
```

To change that, specify the location when you run cmake.
For example, the following will install in /usr/local/lrose/bin:

```
  cmake -DCMAKE_INSTALL_PREFIX=/usr/local/lrose ..
```

