# Partitioning

Disk partitioning simply means creating regions of memory on a storage device, so they can be managed separately.

A disk may be allocated on a single or multiple partitions for dual booting, having a swap partition, or separating audio and video files: the partitioning scheme lives in a partition table such as MBR or GPT.

- About swap: Swapping is a process wherein a page of memory is copied to specified space on the hard disk, to free up the memory, with swap space being a portion of the total available virtual memory.
- A partition table is a table that lives on disk, and describes it's partitions.

Partitions typically contain a file system directly, and any block device (such as a partition) that contains such a file system, is a volume.

## Partition Table

The main partition table types are Master Boot Record and GUID 