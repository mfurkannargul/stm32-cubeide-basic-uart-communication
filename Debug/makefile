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
lab8_3.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
lab8_3.list \

OBJCOPY_BIN += \
lab8_3.bin \


# All Target
all: lab8_3.elf secondary-outputs

# Tool invocations
lab8_3.elf: $(OBJS) $(USER_OBJS) C:\Users\furka\STM32CubeIDE\workspace_1.3.0\lab8_3\STM32F107VCTX_FLASH.ld
	arm-none-eabi-gcc -o "lab8_3.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\furka\STM32CubeIDE\workspace_1.3.0\lab8_3\STM32F107VCTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="lab8_3.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

lab8_3.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "lab8_3.list"
	@echo 'Finished building: $@'
	@echo ' '

lab8_3.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "lab8_3.bin"
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
