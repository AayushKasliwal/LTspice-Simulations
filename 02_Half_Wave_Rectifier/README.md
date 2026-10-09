# Experiment 02: Half-Wave Rectifier

## Objective
To simulate a half-wave rectifier using a diode in LTspice and observe how it converts an AC input into a pulsating DC output.

## Components Used
- 1N4148 diode (D1)
- 1 kΩ load resistor (R1)
- Sinusoidal voltage source (V1)
- Ground

## Circuit Description
The sinusoidal input source is connected in series with diode D1 and load resistor R1. The output voltage is measured across the load resistor.

## Component Values
- Input source: `SINE(0 5 1000)` — 5 V peak, 1 kHz
- Diode: `1N4148`
- Load resistor: `1 kΩ`

## Simulation Settings
- Analysis: Transient
- Stop time: `5m`
- Maximum timestep: `10u`
- Simulation command: `.tran 0 5m 0 10u`

## Waveforms
- `V(VIN)` — input sinusoidal waveform
- `V(VOUT)` — rectified output waveform

## Observations
- The input voltage is a sinusoidal AC waveform.
- The diode conducts during positive half-cycles when forward-biased.
- During negative half-cycles, the diode blocks current, so the output remains close to 0 V.
- The output peak is lower than the input peak by approximately the diode's forward voltage. In the completed simulation, the output peak was around 4.3 V for a 5 V input peak.

## Result
The half-wave rectifier was simulated successfully in LTspice. The output is a pulsating DC waveform consisting mainly of the positive half-cycles of the input signal.

## Files
- `02_Half_Wave_Rectifier.asc` — LTspice schematic
- `02_Half_Wave_Rectifier.plt` — saved plot settings, if included
- `02_Half_Wave_Rectifier_Result.png` — combined circuit and waveform screenshot
