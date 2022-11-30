# Hey! I'm Filing Here

This program implements a 1 MiB ext2 filesystem with 2 directories, 1 regular file, and 1 symbolic link.

## Building

To build the program, enter the lab4 directory, which should contain ext2-create.c and the MAKEFILE, and run the command "make clean && make".

## Running

To create the base image, run the command "./ext2-create". To create the mount directory and mount the filesytem, run the command "mkdir mnt && sudo mount -o loop cs111-base.img mnt". Running the command "ls -ain" in the mount directory should produce an output that resembles the following:

total 7
  2 drwxr-xr-x 3    0    0 1024 Dec 31  1969 .
610 drwxr-xr-x 5 1000 1000 4096 Nov 29 14:52 ..
 13 lrw-r--r-- 1 1000 1000   11 Dec 31  1969 hello -> hello-world
 12 -rw-r--r-- 1 1000 1000   12 Dec 31  1969 hello-world
 11 drwxr-xr-x 2    0    0 1024 Nov 29 14:52 lost+found

## Cleaning up

To unmount the filesystem and remove the mount directory, run the command "sudo umount mnt && rmdir mnt". To clean up the binary files, run the command "make clean".
