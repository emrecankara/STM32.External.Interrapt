################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
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
EXTERNAL_INTERRAPT.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
EXTERNAL_INTERRAPT.list \

OBJCOPY_BIN += \
EXTERNAL_INTERRAPT.bin \


# All Target
all: EXTERNAL_INTERRAPT.elf secondary-outputs

# Tool invocations
EXTERNAL_INTERRAPT.elf: $(OBJS) $(USER_OBJS) C:\Users\Casper\STM32CubeIDE\workspace_1.3.0\EXTERNAL_INTERRAPT\STM32F407VGTX_FLASH.ld
	arm-none-eabi-gcc -o "EXTERNAL_INTERRAPT.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\Casper\STM32CubeIDE\workspace_1.3.0\EXTERNAL_INTERRAPT\STM32F407VGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="EXTERNAL_INTERRAPT.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

EXTERNAL_INTERRAPT.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "EXTERNAL_INTERRAPT.list"
	@echo 'Finished building: $@'
	@echo ' '

EXTERNAL_INTERRAPT.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "EXTERNAL_INTERRAPT.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
