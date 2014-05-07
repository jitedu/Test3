Test3
=====

实训三 /研讨2
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
test3_old.c:6:21: Storage ptr becomes null

Finished checking --- 2 code warnings

changed:
After my mallocking some space in my original pointer,the segment fault has been solved. 
