# harpoon - fast, simple, and header-only FIX parser for Kraken

Simple header only parser. Define a handler with what to do with the fields, include harpoon.h, and start parsing!

Designed for streams: Feed bytes to parser, it does the rest. 

Uses SIMD intrinsics for fast scanning.

### Example
Benchmarked with perf.

fileparse.cc parses a 210MB FIX feed of ~1000000 FIX messages, gets a field and sums + averages values in ~174ms.
5.75 million messages/s, or 1.2GB/s on an Intel(R) Core(TM) i5-8500 CPU @ 3.00GHz.
