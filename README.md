# History of UNIX Design and Interfaces

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/80x15.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

This document is an attempt to capture the history of UNIX design and interfaces from its inception in 1969 until today.
We aim to answer the question of when specific parts of UNIX design and interfaces were introduced, and why.
We use a liberal definition of UNIX in this document -- IOW, we include all UNIX-like operating systems (including Linux) and make no difference between POSIX and UNIX.

If you find something that is inaccurate, or you want to add something, please send a pull request!

## Prelude

### 1964

* The Multics project is started. Ken Thompson, and others, were working on Multics before creating UNIX [Salus, 1994].

## UNIX at Bell Labs

### 1969

* Bell Labs withdraws from the Multics project, leaving Ken Thompson (and others) without an interactive, time-sharing operating system.
* Ken Thompson writes the first version of UNIX on PDP-7 in the summer of 1969 [Salus, 1994].

### 1970

* PDP-11 arrives to Bell Labs and UNIX is ported to it.

### 1971

* 1st Edition UNIX is released in November.

### 1972

* 2nd Edition UNIX is released in June.

### 1973

* 3rd Edition UNIX is released in February.
* Ken Thompson presents UNIX at SOSP in October 1973.
* 4th Edition UNIX is released in November. This is the first version of UNIX written in C.

### 1974

* First paper on UNIX, "The UNIX Time-Sharing System" by Dennis M. Ritchie and Ken Thompson, is published in the "Communications of the ACM" in July 1974.

## UNIX at Berkeley

### 1975

* Ken Thompson takes a sabbatical from Bell Labs, joins Berkeley as a visiting professor, and helps install V6 UNIX.

### 1978

* Bill Joy releases Berkeley Software Distribution (BSD) in March 1978.
* V7 UNIX is released.

### 1979

* 3BSD is released. The `vfork` system call is introduced. Virtual memory is paging-based [[Babaoglu and Joy, 1981](https://dl.acm.org/citation.cfm?id=806595)].

### 1980

* 4.0BSD is released.

### 1981

* 4.1BSD is released.

### 1983

* 4.2BSD released in September 1983 with networking (BSD sockets), new filesystem, redesigned system interface, and new signal interface. The 4.2BSD release also introduces the `mmap` system call interface, but does not implement it fully [[Gingell _et al._, 1987]](http://kos.enix.org/pub/gingell8.pdf).
* UNIX System V Release 1 is released. Interprocess communications (IPC) (semaphores, message queues and shared memory) were added [[System V Definition](http://www.linfo.org/system_v.html)].

### 1986

* 4.3BSD released.

## UNIX and POSIX

### 1988

* 4.3BSD-Tahoe is released.
* IEEE Std 1003.1-1988 ("POSIX") released in 1988.
* SunOS 4.0 is released in December 1988. Virtual memory subsystem is rewritten to support shared-memory with `mmap` [[Gingell _et al._, 1987]](http://kos.enix.org/pub/gingell8.pdf).

### 1989

* System V Release 4 (SRv4) is released.

### 1990

* 4.3BSD-Reno is released.

### 1991

* Linux released in September 1991

### 1992

* 386BSD released

### 1993

* 4.4BSD released. Last major Berkeley UNIX release.
* POSIX.1b released: Asynchronous I/O, process scheduling, high-precision clocks and timers, and interprocess communication using semaphores, shared memory, and message queues (now deprecated).

### 1995

* POSIX.1c released: Threads

## Beyond POSIX

### 2000

* POSIX.1g released: Network APIs (including sockets)
* FreeBSD introduces the Kqueue interface [[Lemon, 2000](https://people.freebsd.org/~jlemon/papers/kqueue.pdf)]

## References

* [System V Definition](http://www.linfo.org/system_v.html)
* [The Unix Heritage Society](https://www.tuhs.org/)
* Marshall Kirk McKusick, Keith Bostic, Michael J. Karels, and John Quarterman. [The Design and Implementation of the 4.4 BSD Operating System ](https://www.amazon.com/Implementation-Operating-paperback-Addison-wesley-Systems/dp/0132317923). 1996.
* Michael Kerrisk. [The Linux Programming Interface: A Linux and UNIX System Programming Handbook](https://www.amazon.com/Linux-Programming-Interface-System-Handbook-ebook/dp/B004OEJMZM). 2010.
* Marshall Kirk McKusick. [Twenty Years of Berkeley Unix - From AT&T-Owned to Freely Redistributable](https://www.oreilly.com/openbook/opensources/book/kirkmck.html). 1999.
* Eric S. Raymond [The Art of Unix Programming](http://www.catb.org/esr/writings/taoup/). 2003.
* Peter H. Salus. [A Quarter Century of UNIX](https://www.amazon.com/Quarter-Century-UNIX-Peter-Salus/dp/0201547775). 1994.
