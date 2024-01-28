# llama2-mac68k.c

I am currently attempting to port llama2.c to classic Macintosh System 7 (THINK C 5.0, C89). This means:

– Porting llama2.c to C89;

– Writing polyfills for unsigned long long, and some floating-point functions in C99 math.h,

– Back-porting stdint.h and time.h from Retro68's C99 implementation;

– Writing polyfills for mmap;

– Handling little-ending (x86_64, AAarch64) to big-endian (68k) conversion when files are read directly into memory;

– (We assume that ints are 4 bytes long, and doubles are 8 bytes long);

Regardless of whether I succeed or not, I'll post things here at some point.
