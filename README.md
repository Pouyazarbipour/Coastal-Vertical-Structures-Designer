# Coastal Vertical Structures Designer

## Overview  
**Coastal Vertical Structures Designer** is a standalone Windows application (`.exe`) for the design and stability analysis of vertical coastal structures such as seawalls and caisson breakwaters. It uses the well-established **Goda wave force formula** to compute design loads.

---

## Input Parameters

The software requires the following **input variables**:

| Variable | Description | Unit | Required |
|----------|-------------|------|----------|
| `Hs` | Significant wave height | m | ✅ |
| `T` | Wave period (typically peak or significant period) | s | ✅ |
| `h` | Water depth at the toe of the structure | m | ✅ |
| `B` | Width of the vertical wall (caisson) | m | ✅ |
| `Rc` | Crest freeboard (height above SWL) | m | ✅ |
| `rho` | Water density | kg/m³ (default: 1025) | ❌ |
| `g` | Gravitational acceleration | m/s² (default: 9.81) | ❌ |
| `wave_type` | Regular or Irregular wave condition | - | ✅ |
| `gamma_b` | Wave breaking coefficient (if wave breaking is modeled) | - | ❌ |

Inputs can be entered via:
- GUI form (in `.exe` version)
- Excel input file (optional, e.g., `input.xlsx`)

---

## Output Parameters

After performing calculations based on the Goda formula, the software generates the following **output values**:

| Output | Description | Unit |
|--------|-------------|------|
| `Pmax` | Maximum wave pressure on the structure | kN/m² |
| `Ftotal` | Total wave force acting on the wall | kN |
| `Zmax` | Location of maximum pressure (from base) | m |
| `M` | Resulting moment about base of structure | kN·m |
| `Stability_Status` | Pass/Fail status based on safety criteria | - |
| `Pressure_Diagram` | Visualization of pressure distribution | Plot |

Outputs can be:
- Displayed on the GUI window
- Exported to Excel file (`output.xlsx`)
- Saved as plot images (e.g., `pressure_diagram.png`)

---

## Usage Instructions

1. **Download and run** `Coastal_Vertical_Structures_Designer.exe`
2. Enter input variables manually or upload an Excel file
3. Click **"Calculate"**
4. View results in the application or export them

---

## Methodology

This tool is based on the method developed by **Professor Goda**, which calculates wave pressure distribution using both hydrostatic and dynamic components, considering wave breaking, wave setup, and structure geometry.

---

## System Requirements

- Windows 10/11 (64-bit)
- No need for Python or additional packages
- Excel (optional, for input/output)

---

## License  
This project is licensed under the MIT License. See the `LICENSE` file for details.  

---

## Contact  
For questions or feedback, please reach out to pouyazarbipour@gmail.com.

