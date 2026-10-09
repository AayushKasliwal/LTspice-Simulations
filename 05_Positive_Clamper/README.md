# Experiment 05: Positive Clamper

## Objective
To simulate a positive clamper circuit in LTspice and observe how it shifts an AC input waveform in the positive direction.

## Components Used
- 1N4148 diode (D1)
- 100 nF capacitor (C1)
- 100 kΩ resistor (R1)
- Sinusoidal voltage source (V1)
- Ground

## Circuit Description
The sinusoidal input is connected to the output through a series capacitor. A resistor and diode are connected between the output node and ground. The diode's anode is connected to ground and its cathode is connected to the output node.

## Component Values
- Input source: `SINE(0 5 1000)` — 5 V peak, 1 kHz
- Diode: `1N4148`
- Capacitor: `100nF`
- Resistor: `100kΩ`

## Simulation Settings
- Analysis: Transient
- Stop time: `50m`
- Maximum timestep: `10u`
- Simulation command: `.tran 0 50m 0 10u`

## Waveforms
- `V(VIN)` — input sinusoidal waveform
- `V(VOUT)` — positively shifted output waveform

## Observations
- The input waveform oscillates approximately between −5 V and +5 V.
- The output waveform shifts upward, with its negative peak clamped near −0.7 V.
- The output may take a few cycles to settle because the capacitor charges during the simulation startup.
- The final output is approximately −0.7 V to +9.3 V, depending on the diode model and circuit conditions.

## Result
The positive clamper was simulated successfully in LTspice. The output waveform is shifted in the positive direction relative to the input.

## Files
- `05_Positive_Clamper.asc` — LTspice schematic
- `05_Positive_Clamper.plt` — saved plot settings, if included
- `05_Positive_Clamper_Result.png` — combined circuit and waveform screenshot
