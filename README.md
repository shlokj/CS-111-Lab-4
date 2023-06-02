## UID: 905754103

# Hey! I'm Filing Here

This lab aims to implement a stripped-down version of the EXT2 filesystem. It totals 1MiB and consists of 2 directories, 1 regular file, and 1 symbolic link to the regular file.

## Building

To build the `ext2-create` executable, first run `make`.

To create the actual file system image (`cs111-base.img`) using this executable, simply run it: `./ext2-create`.

## Running

We have already run `make` and `./ext2-create` previously. To mount it in a separate directory, first create one:

```
mkdir mnt
```

To mount the filesystem in this directory, run

```
sudo mount -o loop cs111-base.img mnt
```

Then, change directories to enter `mnt`:

```
cd mnt
```

Finally, run `ls -ain`:

<img width="650" alt="image" src="https://github.com/shlokj/cs111-lab4/assets/34567765/3a8e16b8-8d89-41d6-8379-d0a8b926914a">

Similarly, one directory above:

<img width="650" alt="image" src="https://github.com/shlokj/cs111-lab4/assets/34567765/a18a0474-cd19-4e22-af1d-4f26c32f63d0">

## Cleaning up

To unmount the filesystem, first exit the `mnt` directory if you are in it:

```
cd ..
```

Then run
```
sudo umount mnt
```

To remove all generated files, i.e., .o files, the image, and the tarball, run

```
make clean
```
