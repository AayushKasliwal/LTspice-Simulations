# Experiment 09: CMOS Inverter

## Aim
To study the voltage transfer characteristics of a CMOS inverter using LTspice.

## Software Used
- LTspice

## Components Used
- BSS84 P-channel MOSFET
- 2N7002 N-channel MOSFET
- 5 V DC supply
- DC input voltage source

## Circuit Description
The CMOS inverter consists of a PMOS transistor connected to the positive supply and an NMOS transistor connected to ground. Their gates are connected together as the input (`VIN`), while their drains are connected together as the output (`VOUT`).

## Simulation Setup
A DC sweep was performed by varying the input voltage from 0 V to 5 V.

**DC Sweep Command:**
```text
.dc Vin 0 5 0.01
```

The output voltage was plotted against the input voltage to obtain the voltage transfer characteristic.

## Observation
- The output voltage decreases as the input voltage increases.
- The simulated output did not reach the expected 0 V low level at the maximum input voltage.
- The result therefore shows the general inverting behaviour, but the output levels require further verification.

## Result
The voltage transfer characteristic of the CMOS inverter was obtained in LTspice. The observed output levels were documented, and the simulation requires further verification for a fully correct logic-level response.

## Files Included
- `09_CMOS_Inverter.asc` — LTspice schematic
- `09_CMOS_Inverter.plt` — Plot settings, if saved
- `09_CMOS_Inverter_Result.png` — Combined circuit and simulation screenshot
- `README.md` — Experiment documentation
