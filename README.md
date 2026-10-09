# Experiment 01: Diode V--I Characteristics

## Objective

To simulate the voltage-current (V--I) characteristics of a 1N4148 diode
using LTspice and observe its forward- and reverse-bias behavior.

## Components Used

-   1N4148 diode (D1)
-   1 kΩ resistor (R1)
-   DC voltage source (V1)
-   Ground

## Circuit Description

The DC voltage source, resistor, and diode are connected in series. The
source voltage is swept from negative to positive values to observe the
diode current under reverse and forward bias.

## Simulation Settings

-   Resistor: 1 kΩ
-   DC sweep source: V1
-   Start voltage: −10 V
-   Stop voltage: +10 V
-   Voltage increment: 0.01 V
-   Simulation command: `.dc V1 -10 10 0.01`

## Waveform

The diode current is plotted against the voltage across the diode.

-   **X-axis:** Diode voltage, V_D
-   **Y-axis:** Diode current, I_D

## Observations

-   Under reverse bias, the current remains very small over the
    simulated voltage range.
-   Under forward bias, the current rises rapidly after the diode's
    forward-voltage knee, typically around 0.6--0.7 V.
-   The series resistor limits the current through the diode.

## Result

The V--I characteristics of the 1N4148 diode were simulated in LTspice.
The graph shows the diode's forward-conduction behavior and its very
small reverse current.

## Files

-   `01_Diode_VI_Characteristic.asc` --- LTspice circuit schematic
-   `01_Diode_VI_Characteristic_Result.png` --- Combined circuit and
    waveform screenshot
