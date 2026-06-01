Motor Fault Detection PCB
A custom-designed two-layer PCB built around the RP2040 microcontroller that samples vibration and motion data from a Bosch BMI088 IMU, runs an on-device TinyML model to classify brushed DC motor faults in real time, and drives the motor under test directly from the board — all designed from scratch in Altium Designer.
What it does
This board takes 5V from a USB-C input, passes it directly to a DRV8833 motor driver to run the brushed DC motor, and steps it down to a clean 3.3V via a TPS563201 synchronous buck converter for the RP2040 and onboard sensors. The BMI088 IMU continuously captures high-frequency accelerometer and gyroscope data from the motor, which the RP2040 feeds into a quantized TFLite model to detect fault conditions such as bearing wear, rotor imbalance, and mechanical misalignment — without any external compute required.
Key features

5V USB-C power input with CC resistor negotiation and ferrite bead filtering
TPS563201 synchronous buck converter → clean 3.3V regulated supply for MCU and sensors
Motor rail runs directly off 5V VBUS for full-voltage motor drive
DRV8833 brushed DC motor driver with PWM speed and direction control
Bosch BMI088 6-axis IMU (separate accel + gyro dies) for high-fidelity vibration capture
RP2040 dual-core MCU — one core for sensor sampling, one for TFLite inference
W25Q16 16Mb QSPI external flash for model and data storage
On-device fault classification with no PC or cloud dependency
Designed in Altium Designer
