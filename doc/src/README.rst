.. Main project page for ``stringsext``




============
 stringsext
============



-------------------------------------------------------------------
stringsext - search for multi-byte encoded strings in binary data.
-------------------------------------------------------------------


:Author: Jens Getreu
:Copyright: Apache 2 license




**stringsext** is a Unicode enhancement of the *GNU strings* tool with
additional functionalities: **stringsext** recognizes Cyrillic, CJKV
characters and other scripts in all supported multi-byte-encodings,
while *GNU strings* fails in finding any of these scripts in UTF-16 and
many other encodings.

**stringsext** prints all graphic character sequences in *FILE* or
*stdin* that are at least *MIN* bytes long.

Unlike *GNU strings* **stringsext** can be configured to search for
valid characters not only in ASCII but also in many other input
encodings, e.g.: utf-8, utf-16be, utf-16le, big5-2003, euc-jp, koi8-r
and many others. The option **--list-encodings** shows a list of valid
encoding names based on the WHATWG Encoding Standard. When more than one
encoding is specified, the scan is performed in different threads
simultaneously.

When searching for UTF-16 encoded strings, 96% of all possible two byte
sequences, interpreted as UTF-16 code unit, relate directly to a Unicode
code point. As a result, the probability of encountering valid Unicode
characters in a random byte stream, interpreted as UTF-16, is also 96%.
In order to reduce this big number of false positives, **stringsext**
provides a parameterizable Unicode-block-filter. See **--encodings**
option in the manual page for more details.

**stringsext** is mainly useful for determining the Unicode content of
non-text files.

When invoked with ``stringsext -e ascii -c i`` **stringsext** can be
used as *GNU strings* replacement.

Documentation
=============

User documentation
    `manual
    page <http://getreu.net/public/downloads/doc/stringsext/./doc/build/stringsext--man.html>`__

Developer documentation
    `API
    documentation <http://getreu.net/public/downloads/doc/stringsext/./target/doc/stringsext/index.html>`__

Source code
===========

Repository
    `stringsext on Github <https://github.com/getreu/stringsext>`__

Distribution
============

Binaries
    `stringsext
    binaries <http://getreu.net/public/downloads/doc/stringsext/./target/>`__

Manual page
    `stringsext.1 <http://getreu.net/public/downloads/doc/stringsext/./man/stringsext.1>`__

