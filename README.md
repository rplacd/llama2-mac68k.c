# llama2-mac68k.c

I am currently attempting to port llama2.c to classic Macintosh System 7 (THINK C 5.0, C89). This means:

– Rewriting llama2.c in C89 (hoisting up variables, etc.)

– Writing portable polyfills for mmap, types like unsigned long long, uint_8, etc., that rely only on C89;

– Writing *non-portable* polyfills for standard library time functions;

– Handling little-endian (x86_64, AAarch64) to big-endian (68k) conversion when files are read directly into memory;

– (We assume that ints are 4 bytes long, and doubles are 8 bytes long);

Regardless of whether I succeed or not, I'll post things here at some point.

There is a significant blocker: how do we allocate significant amounts of memory (say, >32 MB)? It's likely that we'll need to aggressively compact memory allocated via Toolbox functions, have stringent requirements re: logical memory available, etc. Look at how games give themselves as much memory as possible.
