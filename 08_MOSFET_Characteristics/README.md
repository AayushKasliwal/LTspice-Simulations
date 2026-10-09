# Experiment 08: MOSFET Characteristics

## Aim
To study the drain current (\(I_D\)) versus drain-source voltage (\(V_{DS}\)) characteristics of an N-channel MOSFET for different gate-source voltages (\(V_{GS}\)) using LTspice.

## Software Used
- LTspice

## Components Used
- 2N7002 N-channel MOSFET
- DC voltage sources for \(V_{DS}\) and \(V_{GS}\)
- Ground connections

## Simulation Setup
A DC sweep was performed by varying the drain-source voltage while stepping the gate-source voltage.

**DC Sweep Command:**
```text
.dc VDS 0 10 0.1 VGS 1 5 1
```

The drain current, `Id(M1)`, was plotted against the drain-source voltage.

## Observation
- The drain current increases as the drain-source voltage rises.
- Higher gate-source voltages produce higher drain currents.
- The curves show the general transition from the rising region toward a flatter region.

**Note:** The simulated current values depend on the selected MOSFET model and circuit setup. They should not be treated as safe real-world operating currents or used to select hardware operating conditions without checking the device datasheet.

## Result
The drain current versus drain-source voltage characteristics of the 2N7002 MOSFET were obtained for different gate-source voltages using LTspice.

## Files Included
- `08_MOSFET_Characteristics.asc` — LTspice schematic
- `08_MOSFET_Characteristics.plt` — Plot settings
- `08_MOSFET_Characteristics_Result.png` — Combined circuit and simulation screenshot
- `README.md` — Experiment documentation
