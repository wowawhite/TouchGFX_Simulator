################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include TouchGFX/gui/src/screen1_screen/subdir.mk
-include TouchGFX/gui/src/model/subdir.mk
-include TouchGFX/gui/src/common/subdir.mk
-include TouchGFX/generated/texts/src/subdir.mk
-include TouchGFX/generated/images/src/__designer/subdir.mk
-include TouchGFX/generated/images/src/subdir.mk
-include TouchGFX/generated/gui_generated/src/screen1_screen/subdir.mk
-include TouchGFX/generated/gui_generated/src/common/subdir.mk
-include TouchGFX/generated/fonts/src/subdir.mk
-include TouchGFX/build/MINGW32_NT-6.2/touchgfx/framework/source/platform/hal/simulator/sdl2/subdir.mk
-include TouchGFX/build/MINGW32_NT-6.2/touchgfx/framework/source/platform/driver/touch/subdir.mk
-include TouchGFX/build/MINGW32_NT-6.2/simulator/subdir.mk
-include TouchGFX/build/MINGW32_NT-6.2/gui/src/screen1_screen/subdir.mk
-include TouchGFX/build/MINGW32_NT-6.2/gui/src/model/subdir.mk
-include TouchGFX/build/MINGW32_NT-6.2/gui/src/common/subdir.mk
-include TouchGFX/build/MINGW32_NT-6.2/generated/texts/src/subdir.mk
-include TouchGFX/build/MINGW32_NT-6.2/generated/images/src/__designer/subdir.mk
-include TouchGFX/build/MINGW32_NT-6.2/generated/images/src/subdir.mk
-include TouchGFX/build/MINGW32_NT-6.2/generated/gui_generated/src/screen1_screen/subdir.mk
-include TouchGFX/build/MINGW32_NT-6.2/generated/gui_generated/src/common/subdir.mk
-include TouchGFX/build/MINGW32_NT-6.2/generated/fonts/src/subdir.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/portable/MemMang/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/portable/GCC/ARM_CM7/r0p1/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/CMSIS_RTOS/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/subdir.mk
-include Middlewares/Third_Party/FatFs/src/option/subdir.mk
-include Middlewares/Third_Party/FatFs/src/subdir.mk
-include Middlewares/ST/TouchGFX/touchgfx/os/subdir.mk
-include Middlewares/ST/TouchGFX/touchgfx/framework/source/touchgfx/widgets/canvas/subdir.mk
-include Middlewares/ST/TouchGFX/touchgfx/framework/source/touchgfx/widgets/subdir.mk
-include Middlewares/ST/TouchGFX/touchgfx/framework/source/touchgfx/containers/scrollers/subdir.mk
-include Middlewares/ST/TouchGFX/touchgfx/framework/source/touchgfx/containers/progress_indicators/subdir.mk
-include Middlewares/ST/TouchGFX/touchgfx/framework/source/touchgfx/containers/clock/subdir.mk
-include Middlewares/ST/TouchGFX/touchgfx/framework/source/touchgfx/containers/subdir.mk
-include Middlewares/ST/STM32_USB_Host_Library/Core/Src/subdir.mk
-include Middlewares/ST/STM32_USB_Host_Library/Class/CDC/Src/subdir.mk
-include Drivers/STM32F7xx_HAL_Driver/Src/subdir.mk
-include Drivers/BSP/Components/ft5336/subdir.mk
-include Drivers/BSP/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(CC_DEPS)),)
-include $(CC_DEPS)
endif
ifneq ($(strip $(C++_DEPS)),)
-include $(C++_DEPS)
endif
ifneq ($(strip $(C_UPPER_DEPS)),)
-include $(C_UPPER_DEPS)
endif
ifneq ($(strip $(CXX_DEPS)),)
-include $(CXX_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
ifneq ($(strip $(CPP_DEPS)),)
-include $(CPP_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
TouchGFX_Simulator.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
TouchGFX_Simulator.list \

OBJCOPY_BIN += \
TouchGFX_Simulator.bin \


# All Target
all: TouchGFX_Simulator.elf secondary-outputs

# Tool invocations
TouchGFX_Simulator.elf: $(OBJS) $(USER_OBJS) /home/wowa/STM32CubeIDE/workspace_stm/TouchGFX_Simulator/STM32F746NGHX_FLASH.ld
	arm-none-eabi-g++ -o "TouchGFX_Simulator.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m7 -T"/home/wowa/STM32CubeIDE/workspace_stm/TouchGFX_Simulator/STM32F746NGHX_FLASH.ld" --specs=nosys.specs -Wl,-Map="TouchGFX_Simulator.map" -Wl,--gc-sections -static -L../Middlewares/ST/TouchGFX/touchgfx/lib/core/cortex_m7/gcc --specs=nano.specs -mfpu=fpv5-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -lstdc++ -lsupc++ -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

TouchGFX_Simulator.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "TouchGFX_Simulator.list"
	@echo 'Finished building: $@'
	@echo ' '

TouchGFX_Simulator.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "TouchGFX_Simulator.bin"
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
