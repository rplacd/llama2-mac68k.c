# llama2-mac68k.c

I am currently attempting to port llama2.c to classic Macintosh System 7 (THINK C 5.0, C89). This means:

– Porting llama2.c to C89;

– Writing polyfills for unsigned long long, and some floating-point functions in C99 math.h,

– Back-porting stdint.h and time.h from Retro68's C99 implementation;

– and, the part I haven't done yet, polyfilling for mmap.

Regardless of whether I succeed or not, I'll post things here at some point.
