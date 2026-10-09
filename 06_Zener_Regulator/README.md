# Experiment 06: Zener Regulator

## Objective
To simulate a Zener voltage regulator in LTspice and observe how it maintains a nearly constant output voltage as the input voltage changes.

## Components Used
- UDZV6_2B Zener diode (D1)
- 470 Ω series resistor (R1)
- 1 kΩ load resistor (R2)
- DC voltage source (V1)
- Ground

## Circuit Description
The input voltage is connected to the output node through a series resistor. The Zener diode is connected between the output and ground in reverse bias, with its cathode connected to the output node and its anode connected to ground. The load resistor is connected across the output.

## Component Values
- Input voltage sweep: 0 V to 15 V
- Series resistor: 470 Ω
- Load resistor: 1 kΩ
- Zener diode: UDZV6_2B, nominal breakdown voltage approximately 6.2 V

## Simulation Settings
- Analysis: DC sweep
- Swept source: V1
- Start voltage: `0`
- Stop voltage: `15`
- Increment: `0.1`
- Simulation command: `.dc V1 0 15 0.1`

## Waveform
- `V(VOUT)` — output voltage versus input voltage

## Observations
- At low input voltages, the output increases with the input.
- When the Zener diode enters breakdown, the output begins to stabilize near its nominal Zener voltage.
- The output is not perfectly constant because the diode has a finite dynamic resistance and regulation depends on the input and load currents.

## Result
The Zener regulator was simulated in LTspice. The output voltage initially rises with the input and then approaches a regulated level near the Zener diode's breakdown voltage.

## Files
- `06_Zener_Regulator.asc` — LTspice schematic
- `06_Zener_Regulator.plt` — saved plot settings, if included
- `06_Zener_Regulator_Result.png` — combined circuit and waveform screenshot
