# bioptools-binder
bioptools available in Jupyter session served via myBinder.org

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fomightez/bioptools-binder/main)



FAILS CURRENTLY TO RUN VIA MYBINDER
------------------------------------

**Won't build in current state.**

Fails in build now at current end of `make` step with same errors (`error: C++ style comments are not allowed in ISO C90`) as when I tried installing inside a running session:

```text
gcc -fPIC -ansi -Wall -pedantic -g -DGUNZIP_SUPPORT -finline-functions -D XML_SUPPORT -I/srv/conda/include/libxml2 -I/srv/conda/include -o ReadPDB.o -c ReadPDB.c
In file included from /srv/conda/include/libxml2/libxml/encoding.h:31:0,
                 from /srv/conda/include/libxml2/libxml/parser.h:812,
                 from ReadPDB.c:325:
/srv/conda/include/unicode/ucnv.h:1:1: error: C++ style comments are not allowed in ISO C90
 // © 2016 and later: Unicode, Inc. and others.
 ^
/srv/conda/include/unicode/ucnv.h:1:1: error: (this will be reported only once per input file)
In file included from /srv/conda/include/unicode/ucnv.h:52:0,
                 from /srv/conda/include/libxml2/libxml/encoding.h:31,
                 from /srv/conda/include/libxml2/libxml/parser.h:812,
                 from ReadPDB.c:325:
/srv/conda/include/unicode/ucnv_err.h:1:1: error: C++ style comments are not allowed in ISO C90
 // © 2016 and later: Unicode, Inc. and others.
 ^
/srv/conda/include/unicode/ucnv_err.h:1:1: error: (this will be reported only once per input file)
In file included from /srv/conda/include/unicode/ucnv_err.h:88:0,
                 from /srv/conda/include/unicode/ucnv.h:52,
                 from /srv/conda/include/libxml2/libxml/encoding.h:31,
                 from /srv/conda/include/libxml2/libxml/parser.h:812,
                 from ReadPDB.c:325:
/srv/conda/include/unicode/utypes.h:1:1: error: C++ style comments are not allowed in ISO C90
 // © 2016 and later: Unicode, Inc. and others.
 ^
/srv/conda/include/unicode/utypes.h:1:1: error: (this will be reported only once per input file)
In file included from /srv/conda/include/unicode/utypes.h:38:0,
                 from /srv/conda/include/unicode/ucnv_err.h:88,
                 from /srv/conda/include/unicode/ucnv.h:52,
                 from /srv/conda/include/libxml2/libxml/encoding.h:31,
                 from /srv/conda/include/libxml2/libxml/parser.h:812,
                 from ReadPDB.c:325:
/srv/conda/include/unicode/umachine.h:1:1: error: C++ style comments are not allowed in ISO C90
 // © 2016 and later: Unicode, Inc. and others.
 ^
/srv/conda/include/unicode/umachine.h:1:1: error: (this will be reported only once per input file)
In file included from /srv/conda/include/unicode/umachine.h:46:0,
                 from /srv/conda/include/unicode/utypes.h:38,
                 from /srv/conda/include/unicode/ucnv_err.h:88,
                 from /srv/conda/include/unicode/ucnv.h:52,
                 from /srv/conda/include/libxml2/libxml/encoding.h:31,
                 from /srv/conda/include/libxml2/libxml/parser.h:812,
                 from ReadPDB.c:325:
/srv/conda/include/unicode/ptypes.h:1:1: error: C++ style comments are not allowed in ISO C90
 // © 2016 and later: Unicode, Inc. and others.
 ^
/srv/conda/include/unicode/ptypes.h:1:1: error: (this will be reported only once per input file)
In file included from /srv/conda/include/unicode/ptypes.h:52:0,
                 from /srv/conda/include/unicode/umachine.h:46,
                 from /srv/conda/include/unicode/utypes.h:38,
                 from /srv/conda/include/unicode/ucnv_err.h:88,
                 from /srv/conda/include/unicode/ucnv.h:52,
                 from /srv/conda/include/libxml2/libxml/encoding.h:31,
                 from /srv/conda/include/libxml2/libxml/parser.h:812,
                 from ReadPDB.c:325:
/srv/conda/include/unicode/platform.h:1:1: error: C++ style comments are not allowed in ISO C90
 // © 2016 and later: Unicode, Inc. and others.
 ^
/srv/conda/include/unicode/platform.h:1:1: error: (this will be reported only once per input file)
In file included from /srv/conda/include/unicode/platform.h:24:0,
                 from /srv/conda/include/unicode/ptypes.h:52,
                 from /srv/conda/include/unicode/umachine.h:46,
                 from /srv/conda/include/unicode/utypes.h:38,
                 from /srv/conda/include/unicode/ucnv_err.h:88,
                 from /srv/conda/include/unicode/ucnv.h:52,
                 from /srv/conda/include/libxml2/libxml/encoding.h:31,
                 from /srv/conda/include/libxml2/libxml/parser.h:812,
                 from ReadPDB.c:325:
/srv/conda/include/unicode/uconfig.h:1:1: error: C++ style comments are not allowed in ISO C90
 // © 2016 and later: Unicode, Inc. and others.
 ^
/srv/conda/include/unicode/uconfig.h:1:1: error: (this will be reported only once per input file)
/srv/conda/include/unicode/uconfig.h:456:9: warning: extra tokens at end of #endif directive [-Wendif-labels]
 #endif  // __UCONFIG_H__
         ^
In file included from /srv/conda/include/unicode/platform.h:25:0,
                 from /srv/conda/include/unicode/ptypes.h:52,
                 from /srv/conda/include/unicode/umachine.h:46,
                 from /srv/conda/include/unicode/utypes.h:38,
                 from /srv/conda/include/unicode/ucnv_err.h:88,
                 from /srv/conda/include/unicode/ucnv.h:52,
                 from /srv/conda/include/libxml2/libxml/encoding.h:31,
                 from /srv/conda/include/libxml2/libxml/parser.h:812,
                 from ReadPDB.c:325:
/srv/conda/include/unicode/uvernum.h:1:1: error: C++ style comments are not allowed in ISO C90
 // © 2016 and later: Unicode, Inc. and others.
 ^
/srv/conda/include/unicode/uvernum.h:1:1: error: (this will be reported only once per input file)
In file included from /srv/conda/include/unicode/ptypes.h:52:0,
                 from /srv/conda/include/unicode/umachine.h:46,
                 from /srv/conda/include/unicode/utypes.h:38,
                 from /srv/conda/include/unicode/ucnv_err.h:88,
                 from /srv/conda/include/unicode/ucnv.h:52,
                 from /srv/conda/include/libxml2/libxml/encoding.h:31,
                 from /srv/conda/include/libxml2/libxml/parser.h:812,
                 from ReadPDB.c:325:
/srv/conda/include/unicode/platform.h:885:9: warning: extra tokens at end of #endif directive [-Wendif-labels]
 #endif  // _PLATFORM_H
         ^
In file included from /srv/conda/include/unicode/utypes.h:38:0,
                 from /srv/conda/include/unicode/ucnv_err.h:88,
                 from /srv/conda/include/unicode/ucnv.h:52,
                 from /srv/conda/include/libxml2/libxml/encoding.h:31,
                 from /srv/conda/include/libxml2/libxml/parser.h:812,
                 from ReadPDB.c:325:
/srv/conda/include/unicode/umachine.h:313:9: warning: extra tokens at end of #endif directive [-Wendif-labels]
 #endif  // U_DEFINE_FALSE_AND_TRUE
         ^
In file included from /srv/conda/include/unicode/umachine.h:489:0,
                 from /srv/conda/include/unicode/utypes.h:38,
                 from /srv/conda/include/unicode/ucnv_err.h:88,
                 from /srv/conda/include/unicode/ucnv.h:52,
                 from /srv/conda/include/libxml2/libxml/encoding.h:31,
                 from /srv/conda/include/libxml2/libxml/parser.h:812,
                 from ReadPDB.c:325:
/srv/conda/include/unicode/urename.h:1:1: error: C++ style comments are not allowed in ISO C90
 // © 2016 and later: Unicode, Inc. and others.
 ^
/srv/conda/include/unicode/urename.h:1:1: error: (this will be reported only once per input file)
In file included from /srv/conda/include/unicode/utypes.h:39:0,
                 from /srv/conda/include/unicode/ucnv_err.h:88,
                 from /srv/conda/include/unicode/ucnv.h:52,
                 from /srv/conda/include/libxml2/libxml/encoding.h:31,
                 from /srv/conda/include/libxml2/libxml/parser.h:812,
                 from ReadPDB.c:325:
/srv/conda/include/unicode/uversion.h:1:1: error: C++ style comments are not allowed in ISO C90
 // © 2016 and later: Unicode, Inc. and others.
 ^
/srv/conda/include/unicode/uversion.h:1:1: error: (this will be reported only once per input file)
In file included from /srv/conda/include/unicode/utypes.h:44:0,
                 from /srv/conda/include/unicode/ucnv_err.h:88,
                 from /srv/conda/include/unicode/ucnv.h:52,
                 from /srv/conda/include/libxml2/libxml/encoding.h:31,
                 from /srv/conda/include/libxml2/libxml/parser.h:812,
                 from ReadPDB.c:325:
/srv/conda/include/unicode/utf.h:1:1: error: C++ style comments are not allowed in ISO C90
 // © 2016 and later: Unicode, Inc. and others.
 ^
/srv/conda/include/unicode/utf.h:1:1: error: (this will be reported only once per input file)
In file included from /srv/conda/include/unicode/utf.h:217:0,
                 from /srv/conda/include/unicode/utypes.h:44,
                 from /srv/conda/include/unicode/ucnv_err.h:88,
                 from /srv/conda/include/unicode/ucnv.h:52,
                 from /srv/conda/include/libxml2/libxml/encoding.h:31,
                 from /srv/conda/include/libxml2/libxml/parser.h:812,
                 from ReadPDB.c:325:
/srv/conda/include/unicode/utf8.h:1:1: error: C++ style comments are not allowed in ISO C90
 // © 2016 and later: Unicode, Inc. and others.
 ^
/srv/conda/include/unicode/utf8.h:1:1: error: (this will be reported only once per input file)
In file included from /srv/conda/include/unicode/utf.h:218:0,
                 from /srv/conda/include/unicode/utypes.h:44,
                 from /srv/conda/include/unicode/ucnv_err.h:88,
                 from /srv/conda/include/unicode/ucnv.h:52,
                 from /srv/conda/include/libxml2/libxml/encoding.h:31,
                 from /srv/conda/include/libxml2/libxml/parser.h:812,
                 from ReadPDB.c:325:
/srv/conda/include/unicode/utf16.h:1:1: error: C++ style comments are not allowed in ISO C90
 // © 2016 and later: Unicode, Inc. and others.
 ^
/srv/conda/include/unicode/utf16.h:1:1: error: (this will be reported only once per input file)
In file included from /srv/conda/include/unicode/utf.h:221:0,
                 from /srv/conda/include/unicode/utypes.h:44,
                 from /srv/conda/include/unicode/ucnv_err.h:88,
                 from /srv/conda/include/unicode/ucnv.h:52,
                 from /srv/conda/include/libxml2/libxml/encoding.h:31,
                 from /srv/conda/include/libxml2/libxml/parser.h:812,
                 from ReadPDB.c:325:
/srv/conda/include/unicode/utf_old.h:1:1: error: C++ style comments are not allowed in ISO C90
 // © 2016 and later: Unicode, Inc. and others.
 ^
/srv/conda/include/unicode/utf_old.h:1:1: error: (this will be reported only once per input file)
In file included from /srv/conda/include/unicode/utf_old.h:145:0,
                 from /srv/conda/include/unicode/utf.h:221,
                 from /srv/conda/include/unicode/utypes.h:44,
                 from /srv/conda/include/unicode/ucnv_err.h:88,
                 from /srv/conda/include/unicode/ucnv.h:52,
                 from /srv/conda/include/libxml2/libxml/encoding.h:31,
                 from /srv/conda/include/libxml2/libxml/parser.h:812,
                 from ReadPDB.c:325:
/srv/conda/include/unicode/utf.h:1:1: error: C++ style comments are not allowed in ISO C90
 // © 2016 and later: Unicode, Inc. and others.
 ^
/srv/conda/include/unicode/utf.h:1:1: error: (this will be reported only once per input file)
In file included from /srv/conda/include/unicode/utf.h:221:0,
                 from /srv/conda/include/unicode/utypes.h:44,
                 from /srv/conda/include/unicode/ucnv_err.h:88,
                 from /srv/conda/include/unicode/ucnv.h:52,
                 from /srv/conda/include/libxml2/libxml/encoding.h:31,
                 from /srv/conda/include/libxml2/libxml/parser.h:812,
                 from ReadPDB.c:325:
/srv/conda/include/unicode/utf_old.h:1199:9: warning: extra tokens at end of #endif directive [-Wendif-labels]
 #endif  // !U_HIDE_DEPRECATED_API && !U_HIDE_OBSOLETE_UTF_OLD_H
         ^
In file included from /srv/conda/include/unicode/ucnv_err.h:88:0,
                 from /srv/conda/include/unicode/ucnv.h:52,
                 from /srv/conda/include/libxml2/libxml/encoding.h:31,
                 from /srv/conda/include/libxml2/libxml/parser.h:812,
                 from ReadPDB.c:325:
/srv/conda/include/unicode/utypes.h:447:9: warning: extra tokens at end of #endif directive [-Wendif-labels]
 #endif  // U_HIDE_DEPRECATED_API
         ^
/srv/conda/include/unicode/utypes.h:491:9: warning: extra tokens at end of #endif directive [-Wendif-labels]
 #endif  // U_HIDE_DRAFT_API
         ^
/srv/conda/include/unicode/utypes.h:499:9: warning: extra tokens at end of #endif directive [-Wendif-labels]
 #endif  // U_HIDE_DEPRECATED_API
         ^
/srv/conda/include/unicode/utypes.h:546:9: warning: extra tokens at end of #endif directive [-Wendif-labels]
 #endif  // U_HIDE_DEPRECATED_API
         ^
/srv/conda/include/unicode/utypes.h:579:9: warning: extra tokens at end of #endif directive [-Wendif-labels]
 #endif  // U_HIDE_DEPRECATED_API
         ^
/srv/conda/include/unicode/utypes.h:605:9: warning: extra tokens at end of #endif directive [-Wendif-labels]
 #endif  // U_HIDE_DEPRECATED_API
         ^
/srv/conda/include/unicode/utypes.h:641:9: warning: extra tokens at end of #endif directive [-Wendif-labels]
 #endif  // U_HIDE_DEPRECATED_API
         ^
/srv/conda/include/unicode/utypes.h:662:9: warning: extra tokens at end of #endif directive [-Wendif-labels]
 #endif  // U_HIDE_DEPRECATED_API
         ^
/srv/conda/include/unicode/utypes.h:682:9: warning: extra tokens at end of #endif directive [-Wendif-labels]
 #endif  // U_HIDE_DEPRECATED_API
         ^
/srv/conda/include/unicode/utypes.h:690:9: warning: extra tokens at end of #endif directive [-Wendif-labels]
 #endif  // U_HIDE_DEPRECATED_API
         ^
In file included from /srv/conda/include/unicode/ucnv.h:53:0,
                 from /srv/conda/include/libxml2/libxml/encoding.h:31,
                 from /srv/conda/include/libxml2/libxml/parser.h:812,
                 from ReadPDB.c:325:
/srv/conda/include/unicode/uenum.h:1:1: error: C++ style comments are not allowed in ISO C90
 // © 2016 and later: Unicode, Inc. and others.
 ^
/srv/conda/include/unicode/uenum.h:1:1: error: (this will be reported only once per input file)
/srv/conda/include/unicode/uenum.h:30:10: warning: extra tokens at end of #endif directive [-Wendif-labels]
 #endif   // U_SHOW_CPLUSPLUS_API
          ^
In file included from /srv/conda/include/libxml2/libxml/encoding.h:31:0,
                 from /srv/conda/include/libxml2/libxml/parser.h:812,
                 from ReadPDB.c:325:
/srv/conda/include/unicode/ucnv.h:57:10: warning: extra tokens at end of #endif directive [-Wendif-labels]
 #endif   // U_SHOW_CPLUSPLUS_API
          ^
/srv/conda/include/unicode/ucnv.h:954:9: warning: extra tokens at end of #endif directive [-Wendif-labels]
 #endif  // U_HIDE_DEPRECATED_API
         ^
Makefile:126: recipe for target 'ReadPDB.o' failed
make[1]: Leaving directory '/home/jovyan/bioptools/bioptools-1.10/src/libsrc/bioplib/src'
make[1]: *** [ReadPDB.o] Error 1
make: *** [bioplib] Error 2
Makefile:16: recipe for target 'bioplib' failed
Removing intermediate container 350e6ffdffad
The command '/bin/sh -c ./postBuild' returned a non-zero code: 2Built image, launching...
Failed to connect to event stream
```

I cannot see how advice from [here](https://github.com/ACRMGroup/bioptools/issues/14) could be used to make this work via MyBinder.