How to CLI benchmarking of your disk.  
This file give you some useful commands to test the speed for read/write data on your disk. It could be a SSD, HDD, MMC or SD card

I. On Fedora

1. Install the fio (documentation at https://fio.readthedocs.io/en/latest/) program:  
**`# sudo dnf install fio `**
                        
2. Test your disk (in this case /dev/sdb):  
**`# sudo fio -filename=/dev/sdb -direct=1 -iodepth 1 -thread -rw=randrw -ioengine=libaio -bs=512 -size=10M -numjobs=30 -runtime=60 -group_reporting -name=mytest `**

**`-filename`** is the device under test;  
**`-direct`** is a boolean value meaning use/not use of a buffered I/O; direct=0 means use of memory cache which return much larger values then a direct access read/write;  
**`-iodept`** is a number of I/O units to keep in flight against the file;  
**`-thread`** is an option to create jobs by using fork;  
**`-rw`** means to sequential mixed reads and writes;  
**`-ioengine`** defines how the job issues I/O to the file;  
**`-bs`** defines the block size in bytes used for I/O units;  
**`-size`** defines the total size of file I/O for each thread of this job.;  
**`-numjobs`** means to create the specified number of clones of this job; A large numjobs a better read/write estimation value.  
**`-runtime`** is the maximum time for an IO process;  
**`-group_reporting`** display statistics for groups of jobs as a whole instead of for each individual job;  
**`-name`** is the ASCII name of the job;  