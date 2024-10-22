# Partitioning

Disk partitioning simply means creating regions of memory on a storage device, so they can be managed separately.

A disk may be allocated on a single or multiple partitions for dual booting, having a swap partition, or separating audio and video files: the partitioning scheme lives in a partition table such as MBR or GPT.

- About swap: Swapping is a process wherein a page of memory is copied to specified space on the hard disk, to free up the memory, with swap space being a portion of the total available virtual memory.
- A partition table is a table that lives on disk, and describes it's partitions.

Partitions typically contain a file system directly, and any block device (such as a partition) that contains such a file system, is a volume.

## Partition Table

The main partition table types are Master Boot Record and GUID Partition table.

### Master Boot Record

The MBR comprises the first 512 bytes of a storage device, and houses an OS bootloader and the partition table for the device.

The first 440 bytes of MBR are the bootstrap code area, containing the first stage of a bootloader.

In the MBR partition table, partitions are either Primary, Extended, or (Extended) Logical.

- Primary partitions are bootable, and limited to 4 partitions per disk/raid device, however this can be bypassed by making one of the primary partitions and extended partition, containing logical partitions.

Extended partitions are containers for logical partitions, and are limited to one per hard disk: it's counted as a primary, so if one exists, there are only three additional primary partitions available. The number of logical partitions within extended partitions is unlimited.

Primary partitions are labeled `sda1` through `sda4`, with the logical partitions on the last primary being labeled `sda5, sda6` and so on.

### GUID Partition Table

GPT is a partition scheme and is a component of the UEFI specification, using globally unique identifiers to define partitions and partition types: at the start of a GPT, a protective MBR exists to deal with GPT unaware software.

### GPT vs. MBR

GPT is a more modern style of partitioning, and has several advantages over MBR, though the la