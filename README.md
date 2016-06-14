=============
Bro Protosigs
=============

Purely signature based protocol detection for Bro.

This script adds a new field named 'protosig' to the `conn.log` which will 
show the protocol detected by this module.  This script exists as a subset of the full DPD behavior of loose signature matching combined with actual 
protocol parsing to do protocol detection.  There is no protocol parsing 

Write you own signatures
------------------------

1. Create a file named `my-protosigs.sig` in your `site` directory.
2. Add your own signatures to `my-protosigs.sig`.  You can look at the examples shipped with this module and/or refer to the signature documentation here: https://www.bro.org/sphinx/frameworks/signatures.html
3. Load the `my-protosigs.sig` file in local.bro after loading this module like this::
  
  @load bro-protosigs
  @load-sigs my-protosigs.sig

