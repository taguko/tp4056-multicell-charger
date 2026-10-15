# TP4056 Multicell Charger

A USB Type-C powered charger for small 2S/3S LiPo and Li-ion battery packs.

This project was designed to provide a simple and convenient way to charge small multicell batteries without using a full-featured RC balance charger.

## Prototype
![Prototype1 Charge](ima/prototype1_charge.jpg)

## Features

- USB Type-C input
- Supports 2S and 3S LiPo / Li-ion battery packs
- Independent CC/CV charging for each cell
- TP4056-based charging channels
- Isolated DC/DC converters for upper cells
- No conventional balancing circuit required

## Concept

Conventional multicell chargers charge the entire battery pack while balancing cell voltages using a balancing circuit.

This project takes a different approach. Each cell is charged independently using its own TP4056 charger. Isolated DC/DC converters provide separate power domains for upper cells, allowing every cell in the pack to be charged directly to its target voltage.

As a result, cell voltages naturally converge without requiring a conventional balancing circuit.

## Directory Structure

```text
.
├── tp4056-multicell-charger.kicad_sch
├── tp4056-multicell-charger.kicad_pcb
├── Charger_Module.kicad_sym
├── DCDC.kicad_sym
├── Charger_Module.pretty/
└── DCDC.pretty/
```

## Limitations

- This charger assumes that all cells are in reasonable condition and have similar characteristics.
- Cell voltage balance may vary depending on differences in cell aging, internal resistance, capacity, and self-discharge rate.
- Perfect cell balancing under all conditions is not guaranteed.
- This project is intended for users who understand the operating principles and limitations of Li-ion/LiPo charging circuits.
- Users are expected to review the schematic and evaluate the design themselves before use.

## Safety Notice

- For LiPo and Li-ion batteries only.
- Do not use damaged batteries.
- Never leave batteries unattended while charging.
- Do not connect batteries to both the 2-cell and 3-cell connectors simultaneously.
- Verify connector polarity before use.
- Use this project at your own risk.

## Intended Use

This project is primarily intended for educational, experimental, and research purposes.

## License

MIT License
