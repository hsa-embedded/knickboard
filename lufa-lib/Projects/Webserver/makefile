#
#             LUFA Library
#     Copyright (C) Dean Camera, 2012.
#
#  dean [at] fourwalledcubicle [dot] com
#           www.lufa-lib.org
#
# --------------------------------------
#         LUFA Project Makefile.
# --------------------------------------

MCU          = at90usb1287
ARCH         = AVR8
BOARD        = USBKEY
F_CPU        = 8000000
F_USB        = $(F_CPU)
OPTIMIZATION = s
TARGET       = Webserver
SRC          = $(TARGET).c Descriptors.c USBDeviceMode.c USBHostMode.c Lib/SCSI.c Lib/DataflashManager.c \
               Lib/uIPManagement.c Lib/DHCPCommon.c Lib/DHCPClientApp.c Lib/DHCPServerApp.c Lib/HTTPServerApp.c \
               Lib/TELNETServerApp.c Lib/uip/uip.c Lib/uip/uip_arp.c Lib/uip/timer.c Lib/uip/clock.c \
               Lib/uip/uip-split.c Lib/FATFs/diskio.c Lib/FATFs/ff.c $(LUFA_SRC_USB) $(LUFA_SRC_USBCLASS)
LUFA_PATH    = ../../LUFA/
CC_FLAGS     = -DUSE_LUFA_CONFIG_HEADER -IConfig/ -ILib/uip/ -ILib/FATFs/
LD_FLAGS     =

# Default target
all:

# Include LUFA build script makefiles
include $(LUFA_PATH)/Build/lufa.core.in
include $(LUFA_PATH)/Build/lufa.sources.in
include $(LUFA_PATH)/Build/lufa.build.in
include $(LUFA_PATH)/Build/lufa.cppcheck.in
include $(LUFA_PATH)/Build/lufa.doxygen.in
include $(LUFA_PATH)/Build/lufa.dfu.in
include $(LUFA_PATH)/Build/lufa.hid.in
include $(LUFA_PATH)/Build/lufa.avrdude.in
include $(LUFA_PATH)/Build/lufa.atprogram.in
