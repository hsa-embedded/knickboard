all:
	clear
	@echo
	make bootloader_16

#firmware:
#	clear
#	sleep 2
#	@echo Bitte dreucken Sie die RST und HWB Taster
#	@echo und lassen sie die HWB Taster 2 s laenger gedrueckt.
#	sleep 2
#	dfu-programmer at90usb1287 erase
#	dfu-programmer at90usb1287 flash --debug 1 firmware.hex
#	dfu-programmer at90usb1287 reset

bootloader_16:
	clear
	sleep 2
	@echo =====================
	@echo Lade Bootlaoder 16
	@echo =====================
	@echo 
	@echo ------------------------------------
	@echo 
	@echo Ueberspiele bootloader
	@echo ----------------------
	avrdude -c avrispv2 -P usb -p atmega32u4  -U flash:w:atmega32u4_bootloader_16mhz.hex
	@echo

getfuse:
	clear
	sudo avrdude -p atmega32u4 -c avrispv2 -P usb -v -U lfuse:r:-:i

help:
	clear
	@echo ==========================================
	@echo Folgende Befehle koennen verwendet werden
	@echo ==========================================
	@echo all -laedt Bootloader "ISP" und anschließend Firmware "USB"
	@echo firmware -laedt nur Firmware "USB"
	@echo bootloader -laedt nur Bootloader
	@echo getfuse -liest die aktuellen Fusebits
	@echo help - 
