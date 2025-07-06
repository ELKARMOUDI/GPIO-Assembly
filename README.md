# STM32(f411 Nucleo) Bare-Metal GPIO Assembly

![A503B403-0D77-419F-AD42-10003630A00F](https://github.com/user-attachments/assets/8357aef1-34ee-4e35-8a55-f6b5b4e3ceaa)

## Description
Assembly code to control GPIO on STM32f4xx (Cortex-M4) without libraries. Configures PA5 as output and sets it high.

## Key Features
- **Direct Register Access**:
  - `RCC_AHB1ENR`: Enable GPIOA clock (bit 0)
  - `GPIOA_MODER`: Set PA5 as output (bits 10:11 = `01`)
  - `GPIOA_ODR`: Drive PA5 high (bit 5)
- **Reference Manual Compliance**:
  - Addresses/offsets from RM0383 Reference Manual (e.g., `GPIOA_BASE=0x40020000`)

## Hardware
- **MCU**: STM32F411 (or any Cortex-M4 with same memory map)
- **Connection**: LED on PA5 (adjust pin in code if needed)
