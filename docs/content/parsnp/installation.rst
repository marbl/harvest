Installation from source
==========

Required for building from source:
----------------------

* 64-bit Linux/*nix or OSX (>= v10.7)
* autoconf && automake && libtool
* gcc (>= v4.2.*)
* OpenMP
* Python (>= 2.6.*)

Build (local)
-------------

For your convenience, precompiled binaries provides at::

    http://github.com/marbl/harvest

otherwise, to install from source::

    git clone https://github.com/marbl/parsnp.git parsnp_src
    cd parsnp_src

Before you start, if running OSX Mavericks, OpenMP is not supported via Clang, so you will not be able to build the source. You will need to install OpenMP and build gcc with OpenMP support. This can be accomplished a couple of ways:

    * Install Macports, then:
    
       - sudo port install gcc49
       - sudo port select gcc mp-gcc49
       
    * (or) Install Homebrew, then:
    
       -  brew install gcc49
       
    * (or) Build & install gcc from source with OpenMP
    
       - Download & install gcc 4.9
       
          - https://gcc.gnu.org/install/
          
    * (or) Download & install gcc prebuilt binaries with OpenMP support
    
       - http://hpc.sourceforge.net/
    
    * Final suggestion: If issues persist, we recommend using the precompiled binary until OpenMP is natively supported by Clang/OSX (likely to be so in Yosemite)
Once OpenMP support is added, the first (required!) step is to build libMUSCLE::

    cd muscle
    ./autogen.sh
    ./configure --prefix=`pwd`
    make install

Then, build Parsnp::

    cd ..
    ./autogen.sh
    ./configure
    make install

Once both installed (to cwd install by default)::

    export PARSNPDIR=/path/to/parsnp/install
    
Alternative build instructions (requires sudo)
---------------------------------------------------------------

First (important!), build libMUSCLE::

    cd muscle
    ./autogen.sh
    ./configure --prefix=/usr/local/
    sudo make install

Then, build Parsnp::

    cd ..
    ./autogen.sh
    ./configure --prefix=/usr/local/
    sudo make install
