# Experiment 04: Negative Clipper

## Objective
To simulate a negative clipper circuit in LTspice and observe how it clips the negative portion of an input sinusoidal waveform.

## Components Used
- 1N4148 diode (D1)
- 1 kΩ resistor (R1)
- Sinusoidal voltage source (V1)
- Ground

## Circuit Description
The input sinusoidal voltage is applied through a series resistor to the output node. A diode is connected between the output node and ground, with its cathode connected to the output and its anode connected to ground.

## Component Values
- Input source: `SINE(0 5 1000)` — 5 V peak, 1 kHz
- Diode: `1N4148`
- Series resistor: `1 kΩ`

## Simulation Settings
- Analysis: Transient
- Stop time: `5m`
- Maximum timestep: `10u`
- Simulation command: `.tran 0 5m 0 10u`

## Waveforms
- `V(VIN)` — input sinusoidal waveform
- `V(VOUT)` — clipped output waveform

## Observations
- The input is a sinusoidal waveform with positive and negative half-cycles.
- The positive portion of the input passes to the output.
- The negative portion is clipped near the diode's forward voltage, approximately −0.7 V.
- The exact clipping level depends on the diode model and circuit conditions.

## Result
The negative clipper was simulated successfully in LTspice. The output waveform shows the negative portion clipped while the positive portion remains largely unchanged.

## Files
- `04_Negative_Clipper.asc` — LTspice schematic
- `04_Negative_Clipper.plt` — saved plot settings, if included
- `04_Negative_Clipper_Result.png` — combined circuit and waveform screenshot
