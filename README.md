# Sycalib
Sycalib aims to enhance Network I/O performance and provide application transparency on many-core systems. This repository contains the library that dynamically allocates core affinity using the policy below 

 - System call context is separate from application context
 - System call threads are handled by the cores that share the last level cache with the processors that handle the interrupts
 - System call threads can be evenly distributed across all the cores or intensively allocated to only a few cores as long as the load does not exceed the threshold

By assigning core affinity, it improves the scalability of network I/O on many-core systems. In addition, This library overrides the system call library that hooks network I/O system calls to offer fully application transparency. Thus it does not require any modifications of applications and the kernel.

## How to build
this section will be treated after the paper is published
