# kconfig

extraction of kconfig included with Linux kernel source tree


cepharum GmbH was looking for more instant access on kconfig to
conveniently integrate it in a product's installer script. Since 
checking out from Linux kernel source tree is a time-wasting 
process this sparse clone has been started. By running our own 
clone we keep control over ongoing development of kconfig and 
how this affects integrity of our installer script.

> By intention all original code was kept as-is after extracting 
> from kernel sources.


## Compiling

### Prerequisites

Ensure to have proper toolchain on your system. Compiling mconf 
requires C compiler and GNU make at least. In addition you need
to install development files of ncurses library. 

#### Ubuntu 14.04 LTS

Install prerequisites by invoking

    sudo apt-get install gcc make libncurses5-dev


### Invoking

Creating mconf is available using separate Makefile providing 
default target for building mconf executable in this folder.
Simply invoke

    make -f Makefile.cepharum

After that you might instantly run mconf by invoking

    ./mconf <yourconfigfile>
