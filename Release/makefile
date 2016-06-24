################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include subdir.mk
-include arduino/core/subdir.mk
-include Libraries/Wire/utility/subdir.mk
-include Libraries/Wire/subdir.mk
-include Libraries/SoftwareSerial/subdir.mk
-include Libraries/SPI/subdir.mk
-include Libraries/PID_v1/subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C++_DEPS)),)
-include $(C++_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
ifneq ($(strip $(CC_DEPS)),)
-include $(CC_DEPS)
endif
ifneq ($(strip $(INO_DEPS)),)
-include $(INO_DEPS)
endif
ifneq ($(strip $(CPP_DEPS)),)
-include $(CPP_DEPS)
endif
ifneq ($(strip $(PDE_DEPS)),)
-include $(PDE_DEPS)
endif
ifneq ($(strip $(CXX_DEPS)),)
-include $(CXX_DEPS)
endif
ifneq ($(strip $(C_UPPER_DEPS)),)
-include $(C_UPPER_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
AR += \
/Users/joel/workspace/git/controlino_v1/controlino/Release/arduino.ar \

ELF += \
controlino_v1.elf \

EEP += \
controlino_v1.eep \

FLASH_IMAGE += \
controlino_v1.hex \


# All Target
all: controlino_v1

# Tool invocations
controlino_v1: $(FLASH_IMAGE)
	@echo 'Building target: $@'
	@echo 'Printing size:'
	"/Applications/Arduino 1.5.2.app/Contents/Resources/Java/hardware/tools/avr/bin/avr-size" -A "/Users/joel/workspace/git/controlino_v1/controlino/Release/controlino_v1.hex"
	@echo 'Finished building target: $@'
	@echo ' '

/Users/joel/workspace/git/controlino_v1/controlino/Release/arduino.ar: $(AR_OBJ)
	@echo 'Starting archiver'
	"/Applications/Arduino 1.5.2.app/Contents/Resources/Java/hardware/tools/avr/bin/avr-ar" rcs "/Users/joel/workspace/git/controlino_v1/controlino/Release/arduino.ar"   $(AR_OBJ)
	@echo 'Finished building: $@'
	@echo ' '

controlino_v1.elf: $(LINK_OBJ) $(AR)
	@echo 'Starting combiner'
	"/Applications/Arduino 1.5.2.app/Contents/Resources/Java/hardware/tools/avr/bin/avr-gcc" -Os -Wl,--gc-sections -mmcu=atmega2560 -o "/Users/joel/workspace/git/controlino_v1/controlino/Release/controlino_v1.elf"   $(LINK_OBJ) $(AR)  "/Users/joel/workspace/git/controlino_v1/controlino/Release/arduino.ar" "-L/Users/joel/workspace/git/controlino_v1/controlino/Release" -lm
	@echo 'Finished building: $@'
	@echo ' '

controlino_v1.eep: $(ELF)
	@echo 'Create eeprom image'
	"/Applications/Arduino 1.5.2.app/Contents/Resources/Java/hardware/tools/avr/bin/avr-objcopy" -O ihex -j .eeprom --set-section-flags=.eeprom=alloc,load --no-change-warnings --change-section-lma .eeprom=0 "/Users/joel/workspace/git/controlino_v1/controlino/Release/controlino_v1.elf" "/Users/joel/workspace/git/controlino_v1/controlino/Release/controlino_v1.eep"
	@echo 'Finished building: $@'
	@echo ' '

controlino_v1.hex: $(EEP)
	@echo 'Create Flash image (ihex format)'
	"/Applications/Arduino 1.5.2.app/Contents/Resources/Java/hardware/tools/avr/bin/avr-objcopy" -O ihex -R .eeprom "/Users/joel/workspace/git/controlino_v1/controlino/Release/controlino_v1.elf" "/Users/joel/workspace/git/controlino_v1/controlino/Release/controlino_v1.hex"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) $(C_DEPS)$(AR)$(FLASH_IMAGE)$(EEP)$(CXX_DEPS)$(C++_DEPS)$(ELF)$(CC_DEPS)$(INO_DEPS)$(AR_OBJ)$(CPP_DEPS)$(PDE_DEPS)$(LINK_OBJ)$(C_UPPER_DEPS)$(SIZEDUMMY) controlino_v1
	-@echo ' '

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
