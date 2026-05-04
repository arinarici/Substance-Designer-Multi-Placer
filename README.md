# Multi Pattern Placer

A Substance 3D Designer node that allows you to apply independent 2D placement to up to 10 patterns simultaneously, with interactive control directly in the 2D view.


---

## Features

- 🎯 **Interactive 2D View Control** — Position each pattern directly in the 2D view using draggable points, just like Photoshop
- 🔢 **Up to 10 Patterns** — Connect up to 10 input textures and transform them independently
- 🎛️ **Dynamic Input Count** — Use the Pattern Count slider to show only the inputs you need
- 🔄 **Per-Pattern Transform** — Each pattern has its own Position, Rotation, and Scale controls
- ↩️ **Reset Positions** — Reset all patterns to their default positions with a single click

---

## Requirements

- Adobe Substance 3D Designer (latest version recommended)
- Use as **SBS** file — SBSAR format does not support dynamic input connectors

---

## Installation

1. Download the `.sbs` file
2. Open Substance 3D Designer
3. Drag and drop the `.sbs` file into your project, or go to **File → Import**
4. Use it as a subgraph in your compositing graph

---

## How to Use

1. **Add the node** to your graph
2. **Set Pattern Count** — Use the slider to choose how many patterns you need (1–10)
3. **Connect your textures** to the Input connectors (P1, P2, P3...)
4. **Position in 2D View** — Select the node, open the 2D view, and drag the points to position each pattern
5. **Adjust Rotation** — Use the Rotation slider for each pattern


---

## Parameters

| Parameter | Type | Description |
|---|---|---|
| Pattern Count | Integer (1–10) | Number of active patterns |
| Offset P1–P10 | Float2 / Position | Position of each pattern (interactive in 2D view) |
| Rotation P1–P10 | Float / Angle | Rotation of each pattern |
| Reset Positions | Boolean | Reset all patterns to default positions |

---

## Known Limitations

- **SBSAR not supported** — Dynamic input connectors require the SBS format. When exported as SBSAR, input connectors will not open dynamically
- Gizmo rotation pivot is based on each pattern's position

---

## Notes

This node was created to replicate the workflow of transforming multiple elements interactively in 2D, similar to working in Photoshop. The 2D view point control is achieved by exposing Position-type Float2 parameters, which appear as draggable points in the Substance Designer 2D view.

---

## License

This project is free to use. Feel free to modify and share.
