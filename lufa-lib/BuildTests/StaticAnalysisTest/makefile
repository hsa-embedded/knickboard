#
#             LUFA Library
#     Copyright (C) Dean Camera, 2012.
#
#  dean [at] fourwalledcubicle [dot] com
#           www.lufa-lib.org
#

# Static anlysis of the entire LUFA source tree, using the free cross-platform "cppcheck" tool.

# Path to the LUFA library core
LUFA_PATH         = ../../LUFA/

CPPCHECK_EXCLUDES = FATFs/            \
                    PetiteFATFs/      \
                    uip/
CPPCHECK_INCLUDES = $(patsubst %/,%,$(LUFA_PATH))/CodeTemplates/   \
                    $(patsubst %/,%,$(LUFA_PATH))/../Projects/AVRISP-MKII/

SRC               = $(patsubst %/,%,$(LUFA_PATH))/..

all: begin cppcheck-config cppcheck end

begin:
	@echo Executing build test "StaticAnalysisTest".
	@echo

end:
	@echo Build test "StaticAnalysisTest" complete.
	@echo

%:
	

.PHONY: all begin end

# Include LUFA build script makefiles
include $(LUFA_PATH)/Build/lufa.core.in
include $(LUFA_PATH)/Build/lufa.cppcheck.in