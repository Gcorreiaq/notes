# Scope

- [Linux](#linux)

# Linux

- **ramfs**: ramfs is a very simple filesystem that exports Linux's disk caching mechanisms (page cache and dentry cache) as a dynamically resizable RAM-based filesystem. \
\
With ramfs, there is no backing store. Files written into ramfs allocate dentries and page cache as usual, but there's nowhere to write them to. This means the pages are never marked clean, so they can't be freed by the VM.

- **ramdisk**: the older ram disk mechanism created a synthetic block device out of an area of RAM and used it as backing store for a filesystem. It has a fixed size, as well as the filesystem. Using a ram disk required unnecessarily copying memory from the fake block device into the page cache (and copying changes back out), as well as creating and destroying dentries.

- **tmpfs**: a ramfs derivative called tmpfs was created to add size limits, and the ability to write the data to swap space. Normal users can be allowed write access to tmpfs mounts. \
\
There is always a kernel internal mount which you will not see at all. \
\
You can mount a tmpfs as follows: 
    ``` 
    sudo mount -t tmpfs tmpfs /mnt/your_mount -o size=10g
    ```

- **initramfs**: It is a gzipped "cpio" format archive which is extracted into rootfs when the kernel boots up. After extracting, the kernel checks to see if rootfs contains a file "init", and if so it executes it as PID 1. If found, this init process is responsible for bringing the system the rest of the way up, including locating and mounting the real root device (if any). \
\
The initramfs archive is linked into the linux kernel image (the directory linux-*/usr is devoted to generating the archive during the build).

- **losetup**: losetup is used to associate loop devices with regular files or block devices. Usage:
    ```
    losetup --find 
    # find the first unused loop device, in this case /dev/loop0

    losetup /dev/loop0 file.img
    mount /dev/loop0 /mnt/your_mount

    umount /mnt/your_mount
    losetup --detach /dev/loop0

    or

    mount -o loop file.img /mnt/your_mount
    ```

- **character devices and block devices**: Block devices are storage devices that can provide data operations in fixed-size blocks for both reading and writing. It includes the implementation of a buffering mechanism to speed up access during access to read and write, eg: hard disks, USB cameras. \
\
Character devices are devices whose driver communicates by sending and receiving single characters (bytes, octets) eg: serial ports, parallel ports, sound cards. The response time and processing speed are faster than the block devices. On the other hand, memory access is required for file access in blocking devices, where files need to be mapped in memory, and the speed difference between memory and block devices can cause performance issues.
