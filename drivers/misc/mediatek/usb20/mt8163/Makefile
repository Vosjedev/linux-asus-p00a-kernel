#
# for USB OTG silicon based on Mentor Graphics INVENTRA designs
#
#include $(srctree)/drivers/misc/mediatek/Makefile.custom
ccflags-$(CONFIG_USB_MTK_HDRC) += -I$(srctree)/drivers/misc/mediatek/usb20

#QMU Flags
ccflags-$(CONFIG_MTK_MUSB_QMU_SUPPORT) += -DMUSB_QMU_SUPPORT
##ccflags-$(CONFIG_MTK_MUSB_QMU_SUPPORT) += -DQMU_TASKLET
ccflags-$(CONFIG_MTK_MUSB_HOST_QMU_SUPPORT) += -DMUSB_QMU_SUPPORT_HOST
ccflags-$(CONFIG_MTK_MUSB_HOST_QMU_SUPPORT) += -DMUSB_QMU__HOST_BULK_RX_AUTO_SPLIT

obj-$(CONFIG_USB_MTK_HDRC)	:= usb20.o usb20_phy.o
obj-$(CONFIG_USB_MTK_HDRC)  += usb20_host.o
obj-$(CONFIG_USB_MTK_OTG)   += usb20_otg_if.o
ifeq ($(CONFIG_MTK_AEE_KDUMP),y)
obj-$(CONFIG_USB_MTK_HDRC) += usb_dump.o
endif
