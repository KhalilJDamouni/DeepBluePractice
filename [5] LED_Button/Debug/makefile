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
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
LED_Button.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
LED_Button.list \

OBJCOPY_BIN += \
LED_Button.bin \


# All Target
all: LED_Button.elf secondary-outputs

# Tool invocations
LED_Button.elf: $(OBJS) $(USER_OBJS) /Users/khalildamouni/Desktop/University/Clubs/UTAT/Firmware/DeepBluePractice/LED_Button/STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "LED_Button.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"/Users/khalildamouni/Desktop/University/Clubs/UTAT/Firmware/DeepBluePractice/LED_Button/STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="LED_Button.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

LED_Button.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "LED_Button.list"
	@echo 'Finished building: $@'
	@echo ' '

LED_Button.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "LED_Button.bin"
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
