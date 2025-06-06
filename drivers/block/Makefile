# SPDX-License-Identifier: GPL-2.0
#
# Makefile for the kernel block device drivers.
#
# 12 June 2000, Christoph Hellwig <hch@infradead.org>
# Rewritten to use lists instead of if-statements.
#

obj-$(CONFIG_MAC_FLOPPY)	+= swim3.o
obj-$(CONFIG_BLK_DEV_SWIM)	+= swim_mod.o
obj-$(CONFIG_BLK_DEV_FD)	+= floppy.o
obj-$(CONFIG_AMIGA_FLOPPY)	+= amiflop.o
obj-$(CONFIG_PS3_DISK)		+= ps3disk.o
obj-$(CONFIG_PS3_VRAM)		+= ps3vram.o
obj-$(CONFIG_ATARI_FLOPPY)	+= ataflop.o
obj-$(CONFIG_AMIGA_Z2RAM)	+= z2ram.o
obj-$(CONFIG_BLK_DEV_RAM)	+= brd.o
obj-$(CONFIG_BLK_DEV_LOOP)	+= loop.o
obj-$(CONFIG_BLK_DEV_DAC960)	+= DAC960.o
obj-$(CONFIG_XILINX_SYSACE)	+= xsysace.o
obj-$(CONFIG_CDROM_PKTCDVD)	+= pktcdvd.o
obj-$(CONFIG_SUNVDC)		+= sunvdc.o
obj-$(CONFIG_BLK_DEV_SKD)	+= skd.o

obj-$(CONFIG_BLK_DEV_UMEM)	+= umem.o
obj-$(CONFIG_BLK_DEV_NBD)	+= nbd.o
obj-$(CONFIG_BLK_DEV_CRYPTOLOOP) += cryptoloop.o
obj-$(CONFIG_VIRTIO_BLK)	+= virtio_blk.o

obj-$(CONFIG_BLK_DEV_SX8)	+= sx8.o

obj-$(CONFIG_XEN_BLKDEV_FRONTEND)	+= xen-blkfront.o
obj-$(CONFIG_XEN_BLKDEV_BACKEND)	+= xen-blkback/
obj-$(CONFIG_BLK_DEV_DRBD)     += drbd/
obj-$(CONFIG_BLK_DEV_RBD)     += rbd.o
obj-$(CONFIG_BLK_DEV_PCIESSD_MTIP32XX)	+= mtip32xx/

obj-$(CONFIG_BLK_DEV_RSXX) += rsxx/
obj-$(CONFIG_ZRAM) += zram/

obj-$(CONFIG_BLK_DEV_NULL_BLK)	+= null_blk.o
null_blk-objs	:= null_blk_main.o
null_blk-$(CONFIG_BLK_DEV_ZONED) += null_blk_zoned.o

skd-y		:= skd_main.o
swim_mod-y	:= swim.o swim_asm.o

obj-$(CONFIG_VSERVICES_BLOCK_SERVER)     += vs_block_server.o
CFLAGS_vs_block_server.o += -Werror
obj-$(CONFIG_VSERVICES_BLOCK_CLIENT)     += vs_block_client.o
CFLAGS_vs_block_client.o += -Werror
