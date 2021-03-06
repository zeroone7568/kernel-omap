#
# Makefile for the linux kernel.
#

# Common support
obj-y := common.o sram.o clock.o devices.o dma.o mux.o \
	 usb.o fb.o io.o counter_32k.o
obj-m :=
obj-n :=
obj-  :=

# OCPI interconnect support for 1710, 1610 and 5912
obj-$(CONFIG_ARCH_OMAP16XX) += ocpi.o

# omap_device support (OMAP2+ only at the moment)
obj-$(CONFIG_ARCH_OMAP2) += omap_device.o
obj-$(CONFIG_ARCH_OMAP3) += omap_device.o
obj-$(CONFIG_ARCH_OMAP4) += omap_device.o
obj-$(CONFIG_REMOTE_PROC) += rproc_user.o

obj-$(CONFIG_OMAP_MCBSP) += mcbsp.o
obj-$(CONFIG_OMAP_RPMSG) += omap_rpmsg.o
obj-$(CONFIG_OMAP_IOMMU) += iommu.o iovmm.o
obj-$(CONFIG_OMAP_IOMMU_DEBUG) += iommu-debug.o

obj-$(CONFIG_OMAP_DM_TIMER) += dmtimer.o
obj-$(CONFIG_OMAP_DEBUG_DEVICES) += debug-devices.o
obj-$(CONFIG_OMAP_DEBUG_LEDS) += debug-leds.o
i2c-omap-$(CONFIG_I2C_OMAP) := i2c.o
obj-y += $(i2c-omap-m) $(i2c-omap-y)

# OMAP mailbox framework
obj-$(CONFIG_OMAP_MBOX_FWK) += mailbox.o

obj-$(CONFIG_OMAP_PM_NOOP) += omap-pm-interface.o
obj-$(CONFIG_OMAP_PM) += omap-pm-interface.o omap-pm-helper.o
obj-$(CONFIG_DSSCOMP) += omap_dsscomp.o
obj-$(CONFIG_ION_OMAP) += sgx_omaplfb.o
