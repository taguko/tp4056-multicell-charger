# TP4056 Multicell Charger

A USB Type-C powered charger for small 2S/3S LiPo and Li-ion battery packs.

This project was designed to provide a simple and convenient way to charge small multicell batteries without using a full-featured RC balance charger.

## Features

- USB Type-C input
- Supports 2S and 3S LiPo / Li-ion battery packs
- Independent CC/CV charging for each cell
- TP4056-based charging channels
- Isolated DC/DC converters for upper cells
- No conventional balancing circuit required

## Concept

Conventional multicell chargers charge the entire battery pack while balancing cell voltages using a balancing circuit.

This project takes a different approach. Each cell is charged independently by its own TP4056 charging circuit. Isolated DC/DC converters provide separate power domains for upper cells, allowing every cell to be charged directly to its target voltage.

As a result, the cell voltages naturally converge without requiring a conventional balancing circuit.

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

## Safety Notice

- For LiPo and Li-ion batteries only.
- Do not use damaged batteries.
- Never leave batteries unattended while charging.
- Do not connect batteries to both the 2-cell and 3-cell connectors simultaneously.
- This charger assumes that all cells are in reasonable condition and have similar characteristics.
- Cell voltage balance may vary depending on differences in cell aging, internal resistance, capacity, and self-discharge rate.
- The author makes no guarantee that perfect cell balancing will be achieved under all conditions.
- This project is intended for users who understand the operating principles and limitations of Li-ion/LiPo charging circuits.
- Users are expected to review the schematic and evaluate the design themselves before use.
- This project is primarily intended for educational, experimental, and research purposes.
- The author assumes no responsibility for any damage resulting from the use of this project.

## Safety Notice

- For LiPo and Li-ion batteries only.
- Do not use damaged batteries.
- Never leave batteries unattended while charging.
- The author assumes no responsibility for any damage resulting from the use of this project.

## License

MIT License
