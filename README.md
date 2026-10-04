# Embedded Systems Course Labs

C driver exercises organized into application, hardware abstraction, microcontroller abstraction, and shared service layers.

## Drivers And Exercises

- GPIO and external interrupts.
- Timer0 and PWM.
- ADC with LM35 sensor exercises.
- UART, SPI, and I2C communication.
- LED and switch hardware abstractions.

## Architecture

| Directory | Responsibility |
| --- | --- |
| `APP/` | Entry point and individual driver test exercises |
| `HAL/` | LED, switch, and LM35 components |
| `MCAL/` | Peripheral drivers and interrupt manager |
| `SERVICES/` | Common types and bit operations |

[`APP/main.c`](APP/main.c) calls the driver exercises. Review the test routines and pin configuration before selecting the exercise to run on hardware.

## Building And Running

Use the compiler, microcontroller target, and hardware configuration appropriate to the register definitions in `MCAL/`. This repository does not include a complete board-specific build or flashing configuration.

An existing GitHub Actions workflow attempts layer checks and C syntax compilation. Hardware behavior requires testing on the target board; a syntax check alone does not validate peripheral operation.
