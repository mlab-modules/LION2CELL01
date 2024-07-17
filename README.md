# LION2CELL01D - Li-ion dual-cell Battery Management Module

![LION2CELL01D](/doc/img/LION2CELL01D_top_big.jpg)

## Description

The LION2CELL01D is an integrated battery management solution for 18650 Li-ion batteries. It is designed to manage the charging, balancing, and monitoring of two series-connected Li-ion cells. This module measures the remaining energy, voltage, and temperature of the batteries, and protects against over-voltage and over-draining conditions.

## Features

- **Charging and Balancing**: Supports charging, balancing, and termination with temperature protection.
- **Gas-gauging**: Temperature-compensated gas-gauging for accurate remaining energy estimation.
- **Protection**: Over-voltage, over-current protection, but no under-voltage protection (the module operates until battery depletion).
- **Communication**: Supports I2C and HDQ communication interfaces.

## Technical Specifications

- **Power Supply**: 12 V @ 2 A
- **Charging Current**: Factory set to approximately 1.3 A
- **Battery Holder**: 2x 18650
- **Interfaces**: I2C, HDQ
- **Integrated Circuits**:
  - BQ24103 for charging
  - BQ34Z100 for fuel gauging
- **Dimensions**: 80.77 x 60.45 x 16 mm

## Connection

| Pin | Signal | Description       |
|-----|--------|-------------------|
| 1   | PG     | Power Good        |
| 2   | STAT2  | Status Indicator  |
| 3   | GND    | Ground            |
| 4   | CE     | Chip Enable       |
| 5   | STAT1  | Status Indicator  |
| 6   | CMODE  | Configuration Mode|

## Construction

The module is constructed with three main functional blocks:
1. **Charging Circuitry**: Manages the charging process of the two series-connected Li-ion cells.
2. **Measurement Circuitry**: Measures the voltage, current, and temperature of the cells.
3. **Balancing and Protection Circuitry**: Ensures cell voltage balancing and provides protection against over-voltage.

### Important Considerations

- Regular charging is required (at least once every six months) to maintain the batteries within operational voltage ranges.
- Specific resistor values and settings are used for the voltage measurement, ensuring accurate readings without exceeding voltage limits.
- The module is equipped with a balancing circuit that discharges one of the cells to match the voltage of the other, with a discharge current around 10 mA.

## Setup and Configuration

1. **Installation**:
   - Check the PCB for proper soldering.
   - Insert the batteries in the designated order: position 1 first, followed by position 2.
   - Verify the operation of the charging function by connecting a 12V adapter.

2. **Software**:
   - Use `setguage2cell.py` to upload parameters to the energy measurement circuit.
   - Parameters are tailored for Panasonic NCR18650B or INR18650MJ1 cells; adjustments are needed for other types.
   - Conduct at least one charge/discharge cycle for accurate energy measurements.
