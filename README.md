# compress.php

Lossless compression of PHP files using 'halt_compiler' and 'gzdeflate'.

### Usage

Copy the code below to a file called 'compress.php' and then on the command line run it like this:

    $ php compress.php api.php 
    compressed 'api.php' from 259 to 41 kbyte (16%)

As you can see compressing 'api.php' reduces it's file size to 16% of the original, which is typical for PHP code and the 'deflate' algorithm. And now run it again:

    $ php compress.php api.php 
    uncompressed 'api.php' from 41 to 259 kbyte (624%)

The script will detect operating on an already compressed file (it looks for the 'halt_compiler' statement) and will automatically switch to uncompression mode. Since the compression is lossless you will end up with the exact same file you started with.
