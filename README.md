Motor Controller PCB
A custom-designed two-layer PCB that accepts a wide range of input voltages (5V–12V), uses a buck converter to regulate a clean 3.3V supply for an onboard microcontroller, and drives a brushed DC motor with full speed and direction control — all on a single board designed in Altium Designer.
What it does
This board takes a variable DC input (5V–12V), steps it down to 3.3V via a synchronous buck converter for stable microcontroller power, while passing the full input voltage directly to a dedicated motor driver IC. The microcontroller generates PWM signals to control motor speed and direction through the motor driver. The design emphasizes proper ground plane separation and power domain isolation between the noisy switching circuitry and sensitive digital logic.
Key features

Wide input voltage range (5V–12V) via buck converter
Buck converter → 3.3V clean regulated MCU supply
Motor rail runs directly off input voltage for maximum torque
Brushed DC motor control with speed and direction via PWM
Onboard STM32/RP2040 microcontroller
Mixed-signal PCB layout with isolated power and logic ground domains
SWD debug header for programming and live debugging
Designed in Altium Designer

Why this matters
Mixed-signal PCB design — where high-current power electronics and sensitive digital logic share the same board — is a foundational skill in embedded systems, defense electronics, robotics, and aerospace hardware. Managing noise, ground plane strategy, and voltage regulation on a single board mirrors the exact challenges found in real-world motor drive systems used in UAVs, actuator control systems, and industrial automation.
More on why this skill set matters in embedded and defense systems: Texas Instruments — Motor Drive & Control Overview


Tools used

Altium (schematic and PCB layout)
STM32CubeIDE / Arduino SDK (firmware)
