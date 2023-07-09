################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
MikroDeney4DOC.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
MikroDeney4DOC.list \

OBJCOPY_HEX += \
MikroDeney4DOC.hex \

OBJCOPY_BIN += \
MikroDeney4DOC.bin \


# All Target
all: MikroDeney4DOC.elf secondary-outputs

# Tool invocations
MikroDeney4DOC.elf: $(OBJS) $(USER_OBJS) C:\Users\yakup\STM32CubeIDE\workspace_1.3.0\MikroDeney4DOC\STM32F103C4TX_FLASH.ld
	arm-none-eabi-gcc -o "MikroDeney4DOC.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\yakup\STM32CubeIDE\workspace_1.3.0\MikroDeney4DOC\STM32F103C4TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="MikroDeney4DOC.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

MikroDeney4DOC.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "MikroDeney4DOC.list"
	@echo 'Finished building: $@'
	@echo ' '

MikroDeney4DOC.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "MikroDeney4DOC.hex"
	@echo 'Finished building: $@'
	@echo ' '

MikroDeney4DOC.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "MikroDeney4DOC.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
