# sanhash
Normalize and hash ASAN/MSAN crash dumps

what
----

When handling crash reports from gcc/clang sanitizers like ASAN/MSAN I often need to
sort through a large list of crashes.

Grouping identical crashes can be annoying due to changing memory addresses and PIDs.
This script will replace changing parts with static values, run it through sha256
and truncate the hash, allowing easier grouping of identical hashes.

Script written by [Hanno Böck](https://hboeck.de).