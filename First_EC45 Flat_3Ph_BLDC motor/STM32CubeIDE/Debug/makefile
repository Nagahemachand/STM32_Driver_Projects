################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (12.3.rel1)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Middlewares/MotorControl/subdir.mk
-include Middlewares/FreeRTOS/subdir.mk
-include Drivers/STM32G4xx_HAL_Driver/subdir.mk
-include Drivers/CMSIS/subdir.mk
-include Application/User/subdir.mk
-include Application/Startup/subdir.mk
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

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := First_EC45 Flat_3Ph_BLDC motor
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
First_EC45\ Flat_3Ph_BLDC\ motor.elf \

MAP_FILES += \
First_EC45\ Flat_3Ph_BLDC\ motor.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
First_EC45\ Flat_3Ph_BLDC\ motor.list \


# All Target
all: main-build

# Main-build Target
main-build: First_EC45\ Flat_3Ph_BLDC\ motor.elf secondary-outputs

# Tool invocations
First_EC45\ Flat_3Ph_BLDC\ motor.elf First_EC45\ Flat_3Ph_BLDC\ motor.map: $(OBJS) $(USER_OBJS) C:\Users\nagah\.st_workbench\projects\First_EC45\ Flat_3Ph_BLDC\ motor\STM32CubeIDE\STM32G431RBTX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "First_EC45 Flat_3Ph_BLDC motor.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\nagah\.st_workbench\projects\First_EC45 Flat_3Ph_BLDC motor\STM32CubeIDE\STM32G431RBTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="First_EC45 Flat_3Ph_BLDC motor.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

First_EC45\ Flat_3Ph_BLDC\ motor.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "First_EC45 Flat_3Ph_BLDC motor.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) First_EC45\ Flat_3Ph_BLDC\ motor.elf First_EC45\ Flat_3Ph_BLDC\ motor.list First_EC45\ Flat_3Ph_BLDC\ motor.map First_EC45\\ Flat_3Ph_BLDC\\ motor.elf default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
