Installation from source
========================

Dependencies:
-------------
   - Autoconf ( http://www.gnu.org/software/autoconf/ )
   - Protocol Buffers ( https://code.google.com/p/protobuf/ )
   - Zlib ( http://www.zlib.net/ )


Build
-----

For your convenience, precompiled binaries provides at::

    http://github.com/marbl/harvest

otherwise, to install from source::

    git clone https://github.com/marbl/harvest-tools.git hvt_src
    cd hvt_src
    
   ./bootsrap.sh
   ./configure [--prefix=...] [--with-protobuf=...]
   make
   [sudo] make install


Products:
---------
   - command line tool ( <prefix>/bin/harvest )
   - static library ( <prefix>/lib/libharvest.a )
   - includes
      - Harvest, Protocol Buffer message class ( <prefix>/include/harvest.pb.h )
      - HarvestIO, Harvest wrapper with file IO ( <prefix>/include/HarvestIO.h )


Additional notes:
-----------------

When running ./configure, use --prefix to install somewhere other than
/usr/local. Use --with-protobuf if the Protocol Buffer libraries are not
in their default location (/usr/local). Zlib should be installed in a standard
system location. Sudo will be necessary for 'make install' if write permission
