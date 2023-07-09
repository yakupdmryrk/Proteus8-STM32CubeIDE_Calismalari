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
mikrodeney4.dc1.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
mikrodeney4.dc1.list \

OBJCOPY_HEX += \
mikrodeney4.dc1.hex \

OBJCOPY_BIN += \
mikrodeney4.dc1.bin \


# All Target
all: mikrodeney4.dc1.elf secondary-outputs

# Tool invocations
mikrodeney4.dc1.elf: $(OBJS) $(USER_OBJS) C:\Users\yakup\STM32CubeIDE\workspace_1.3.0\mikrodeney4.dc1\STM32F103C4TX_FLASH.ld
	arm-none-eabi-gcc -o "mikrodeney4.dc1.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\yakup\STM32CubeIDE\workspace_1.3.0\mikrodeney4.dc1\STM32F103C4TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="mikrodeney4.dc1.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

mikrodeney4.dc1.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "mikrodeney4.dc1.list"
	@echo 'Finished building: $@'
	@echo ' '

mikrodeney4.dc1.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "mikrodeney4.dc1.hex"
	@echo 'Finished building: $@'
	@echo ' '

mikrodeney4.dc1.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "mikrodeney4.dc1.bin"
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
