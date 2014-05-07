Test3
=====

实训三 /研讨2
test3_old.c：



splint debug
错误显示：
witchblade-K43SV D # splint test3_old.c
Splint 3.1.2 --- 03 May 2009

test3_old.c:4:6: Function main declared to return void, should return int
The function main does not match the expected type. (Use -maintype to inhibit
warning)
test3_old.c: (in function main)
test3_old.c:7:13: Null storage ptr passed as non-null param: strcpy (ptr, ...)
A possibly null pointer is passed as a parameter corresponding to a formal
parameter with no /*@null@*/ annotation. If NULL may be used for this
parameter, add a /*@null@*/ annotation to the function parameter declaration.
(Use -nullpass to inhibit warning)
test3_old.c:6:21: Storage ptr becomes n
Finished checking --- 2 code warnings




system_pro_old.c:




valgrind debug
错误显示：
Process terminating with default action of signal 11 (SIGSEGV)
==6045== Access not within mapped region at address 0x0
==6045== at 0x80483FD: main (in /root/.ssh/Test3/system_pro_old)
==6045== If you believe this happened as a result of a stack
==6045== overflow in your program's main thread (unlikely but
==6045== possible), you can try to increase the size of the
==6045== main thread stack using the --main-stacksize= flag.
==6045== The main thread stack size used in this run was 8388608.
==6045==
==6045== HEAP SUMMARY:
==6045== in use at exit: 0 bytes in 0 blocks
==6045== total heap usage: 0 allocs, 0 frees, 0 bytes allocated
==6045==
==6045== All heap blocks were freed -- no leaks are possible
==6045==
==6045== For counts of detected and suppressed errors, rerun with: -v
==6045== ERROR SUMMARY: 1 errors from 1 contexts (suppressed: 0 from 0)
Segmentation fault
访问系统保护的内存引起的错误
changed:
After my mallocking some space in my original pointer,the segment fault has been solved. 
