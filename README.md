Mixed-Signal Motor Control PCB
A custom-designed two-layer PCB that accepts 5V input and delivers full brushed DC motor control alongside onboard voltage regulation for an STM32/RP2040 microcontroller — all on a single board.
What it does
This board takes a 5V source and steps it down to 3.3V through an LDO regulator for clean, stable microcontroller power. A dedicated motor driver IC handles the high-current motor domain, controlled via PWM signals from the onboard MCU. The design emphasizes proper ground plane separation and power domain isolation between the noisy switching circuitry and sensitive digital logic.
Key features

5V input → 3.3V LDO regulation for clean MCU power
Brushed DC motor control with speed and direction via PWM
Onboard STM32/RP2040 microcontroller
Mixed-signal PCB layout with isolated power and logic ground domains
SWD debug header for programming and live debugging
Designed in KiCad

Why this matters
Mixed-signal PCB design — where high-current power electronics and sensitive digital logic share the same board — is a foundational skill in embedded systems, defense electronics, robotics, and aerospace hardware. Managing noise, ground plane strategy, and voltage regulation on a single board mirrors the exact challenges found in real-world motor drive systems used in UAVs, actuator control systems, and industrial automation.
More on why this skill set matters in embedded and defense systems: Texas Instruments — Motor Drive & Control Overview


Tools used

Altium (schematic and PCB layout)
STM32CubeIDE / Arduino SDK (firmware)
