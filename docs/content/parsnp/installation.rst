Installation from source
==========

Required before building:
----------------------

* 64-bit Linux/*nix or OSX (>= v10.7)
* autoconf && automake
* gcc (>= v4.2.*)
* Python (>= 2.6.*)

Build (local)
-------------

For your convenience, precompiled binaries provides at::

    http://github.com/marbl/harvest

otherwise, to install from source::

    git clone https://github.com/marbl/parsnp.git parsnp_src
    cd parsnp_src

First (important!), build libMUSCLE::

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
