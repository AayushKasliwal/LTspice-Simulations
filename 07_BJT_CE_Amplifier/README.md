# Experiment 07: BJT Common-Emitter Amplifier

## Objective
To simulate a BJT common-emitter amplifier using LTspice and observe its input and output waveforms.

## Components Used
- 2N3904 NPN transistor
- 12 V DC supply
- 47 kΩ bias resistor (R1)
- 10 kΩ bias resistor (R2)
- 4.7 kΩ collector resistor (RC)
- 1 kΩ emitter resistor (RE)
- 10 kΩ load resistor (RL)
- 10 µF coupling capacitors (C1 and C2)
- 100 µF emitter-bypass capacitor (CE)

## Circuit Description
The 2N3904 transistor is connected in a common-emitter configuration. R1 and R2 provide base bias, RC is connected to the collector, and RE stabilizes the emitter current. The coupling capacitors transfer the AC input and output signals, while CE bypasses the emitter resistor for AC signals.

## Simulation Settings
- Input signal: `SINE(0 10m 1k)`
- Transient analysis: `.tran 0 10m 0 1u`
- Supply voltage: 12 V DC

## Observations
- The transistor's DC operating point was checked using LTspice.
- The output waveform was plotted alongside the input waveform.
- A common-emitter amplifier is expected to produce an amplified output that is approximately 180° out of phase with the input.
- The output gain and distortion were not independently verified in the final captured waveform.

## Result
The BJT common-emitter amplifier was simulated in LTspice, and its input and output waveforms were observed.

## Files
- `07_BJT_CE_Amplifier.asc` — LTspice circuit schematic
- `07_BJT_CE_Amplifier.plt` — saved plot settings, if included
- `07_BJT_CE_Amplifier_Result.png` — combined circuit and waveform screenshot
