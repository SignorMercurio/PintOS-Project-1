# PintOS-Project-1
Personal solution to PintOS Project 1.

## Note
- Only modified files are uploaded for simplification.
- The format may be untidy in Windows/MacOS, but should be okay in Linux.
- Report is written only in Chinese.
- Parts of code that are hard to understand is explained with comment, but I think most of the code is self-explanatory.
- Modified code starts with ```/* Solution Code */``` so that they're easy to find.
- The name of the function ```checkInvoke()``` might seem strange, because our teacher provide us this one and I don't want to change it.

## What is modified in this project?
- In ```device/```
  - In ```timer.c```:
    - addition: ```timer_interrupt()```
    - modification: ```timer_sleep()```
- In ```threads/```
  - File-addition: ```fixed-point.h```
  - In ```synch.h```:
    - addition: ```struct lock```
    - declaration: ```cond_cmp_priority()```
  - In ```synch.c```:
    - addition: ```sema_down(), sema_up(), lock_release(), cond_signal()```
    - implementation: ```cond_cmp_priority()```
    - modification: ```lock_acquire()```
  - In ```thread.h```
    - addition: ```struct thread```
    - declaration: ```checkInvoke(), thread_cmp_priority(), thread_donate_priority(), thread_hold_lock(), thread_remove_lock(), lock_cmp_priority(), thread_update_priority(), mlfqs_inc_recent_cpu(), mlfqs_update_load_avg_and_recent_cpu(), mlfqs_update_priority()```
    - inclusion: ```"threads/fixed-point.h"```
  - In ```thread.c```
    - addition: ```global variable load_avg, thread_start(), thread_create()```
    - implementation: ```checkInvoke(), thread_cmp_priority(), thread_donate_priority(), thread_hold_lock(), thread_remove_lock(), lock_cmp_priority(), thread_update_priority(), mlfqs_inc_recent_cpu(), mlfqs_update_load_avg_and_recent_cpu(), mlfqs_update_priority(), thread_set_nice(), thread_get_nice(), thread_get_load_avg(), thread_get_recent_cpu()```
    - modification: ```thread_unblock(), thread_yield(), thread_set_priority(), init_thread()```
    
 ## References
 - I cannot install PintOS correctly without [this repo](https://github.com/WyldeCat/pintos-anon).
 - I cannot install bochs correctly without [this page from SourceForge](https://sourceforge.net/projects/bochs/files/bochs/2.6.6/).
 - I cannot figure out how to deal with this project without [this official help](https://web.stanford.edu/class/cs140/projects/pintos/pintos.html).
 - I can make it without my teacher's help, but still I'd like to thank her too.
