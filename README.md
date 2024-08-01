# DC-DC Buck Converter

# Project Overview
This project involves the simulation of a DC-DC buck converter using the LTspice simulation tool. The buck converter steps down a higher input voltage to a lower output voltage, with a specific focus on achieving a 10V output from a 30V input using a 555 timer IC for PWM control.

# Files Included
1. BuckConverter.asc: The LTspice schematic file for the DC-DC buck converter.
2. README.md: This readme file.

# Prerequisites
To run this simulation, you need to have LTspice installed on your computer. You can download LTspice from the Analog Devices LTspice page (https://www.analog.com/en/resources/design-tools-and-calculators/ltspice-simulator.html).

# Schematic Overview
The buck converter circuit consists of the following main components:
  1. 555 Timer IC: Used to generate a PWM signal with a 33.33% duty cycle and a frequency of 40 kHz.
  2. MOSFET (IRF540): Acts as the switching device controlled by the PWM signal from the 555 timer.
  3. Diode (D1): Provides a path for the inductor current when the MOSFET is off.
  4. Inductor (L): Smooths the current flow to the load.
  5. Capacitor (C): Reduces output voltage ripple.
  6. Load Resistor (R): Represents the load connected to the buck converter.

# Component Values
The following component values are used in the schematic:
1. R1 (555 Timer): 10kΩ
2. R2 (555 Timer): 10kΩ
3. C1 (555 Timer): 1.2nF
4. L (Inductor): 5mH
5. C (Output Capacitor): 1.17µF
6. R (Load Resistor): 10Ω
  
# Simulation Instructions
1. Open the Schematic: Open BuckConverter.asc in LTspice.
2. Run the Simulation: Click the "Run" button (the running man icon) to start the simulation.
3. View the Output: Once the simulation is complete, you can view the output voltage by probing the output node in the schematic.

# Adjustments and Fine-Tuning
- Frequency Adjustment: To change the frequency of the PWM signal, adjust the values of R1, R2, and C1 in the 555 timer circuit. The frequency is given by:
    𝑓=1.44/((𝑅1+2𝑅2)𝐶1)
- Duty Cycle Adjustment: To achieve a different duty cycle, adjust the ratio of R1 and R2. The duty cycle is given by:
    𝐷=(𝑅1+𝑅2)/(𝑅1+2𝑅2) 

- Output Voltage: The output voltage of the buck converter is proportional to the duty cycle of the PWM signal. Use the formula:
    𝑉𝑜𝑢𝑡=𝐷×𝑉𝑖𝑛 

# Troubleshooting
- Output Voltage Too Low/High: Check the duty cycle and frequency settings of the 555 timer. Ensure that the component values match the intended design.
- Excessive Ripple: Increase the value of the output capacitor (C2) or use a lower ESR capacitor.
- Simulation Errors: Ensure all component values are correctly placed and there are no open nodes in the schematic.

# Contact
For any questions or issues, please contact Salu Barshad at sbarshad7@gmail.com.
