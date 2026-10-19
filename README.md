# Elecrow ESP32-C3 SuperMini — KiCad Library

Unofficial KiCad symbol and through-hole footprint library for the **white Elecrow ESP32-C3 SuperMini development board**.

> **Hardware verification required:** This library is community-made and is not an official Elecrow design file. The adjacent pin pitch has not been conclusively verified on the physical board. Do not order a PCB until you have measured your exact board and checked the footprint in KiCad.

## Included

- `ESP32-C3-SuperMini_Elecrow.kicad_sym` — schematic symbol with 16 named pins and real electrical connection endpoints.
- `ESP32-C3-SuperMini_Elecrow.pretty/` — two footprint variants:
  - `ESP32-C3-SuperMini_Elecrow_2mm`: based on a reported 2.00 mm adjacent-pin measurement; row centers 18.00 mm apart.
  - `ESP32-C3-SuperMini_Elecrow_2.54mm`: standard 2.54 mm header pitch; row centers 18.60 mm apart.
- `fp-lib-table` — example footprint-library table entry.

## Pin map

Orientation: component side facing you, USB connector at the top.

| Pad | Left row, top to bottom | Pad | Right row, top to bottom |
|---:|---|---:|---|
| 1 | 5V | 9 | GPIO10 |
| 2 | GND | 10 | GPIO9 |
| 3 | 3V3 | 11 | GPIO8 |
| 4 | GPIO20 / RX | 12 | GPIO7 |
| 5 | GPIO21 / TX | 13 | GPIO6 |
| 6 | GPIO2 | 14 | GPIO5 |
| 7 | GPIO1 | 15 | GPIO4 |
| 8 | GPIO0 | 16 | GPIO3 |

The signal labels on footprints are on **F.Fab**, not the silkscreen. The silkscreen marks the USB end as TOP.

## Install

### Schematic symbol

1. In KiCad, open **Preferences → Manage Symbol Libraries**.
2. Choose **Add Existing Library** and select `ESP32-C3-SuperMini_Elecrow.kicad_sym`.
3. Place `ESP32-C3-SuperMini_Elecrow` in the schematic.
4. Confirm the footprint field points to the variant you have physically verified.

### Footprint library

1. Copy the `ESP32-C3-SuperMini_Elecrow.pretty` directory to a stable location.
2. In **Preferences → Manage Footprint Libraries**, add it as a project-specific or global library.
3. Use the library nickname `ESP32-C3-SuperMini_Elecrow`, or update the symbol's footprint field to match your chosen nickname.
4. Assign either `ESP32-C3-SuperMini_Elecrow_2mm` or `ESP32-C3-SuperMini_Elecrow_2.54mm`.

The included `fp-lib-table` is an example; edit its path if you use it.

## Dimensions and fabrication warning

Both variants use a provisional board outline of **21.6 × 25.2 mm**, 1.8 mm circular through-hole pads, and 1.0 mm drills. The 2.00 mm variant uses 2.00 mm adjacent-pad spacing and 18.00 mm row-center spacing. The 2.54 mm variant uses 2.54 mm adjacent-pad spacing and 18.60 mm row-center spacing.

These values are not guaranteed dimensions for every board sold as an ESP32-C3 SuperMini. Measure:
- adjacent pad centers,
- distance between the two row centerlines,
- overall module outline,
- USB connector position and clearance,
- and pin mapping/orientation.

Check the footprint against your actual module and run KiCad's design-rule checks before manufacturing. This library is provided **as-is**, without warranty.

## Reference material

The following Elecrow images were used as visual references for the pin labels and approximate outline. Confirm the links and dimensions against the product revision you own:

- Pin definition: https://media-cdn.elecrow.com/media/webp_image/wysiwyg/products/2024/DES01655M/pin_definition_of_ESP32_C3_dev_board.webp
- Dimension drawing: https://media-cdn.elecrow.com/media/webp_image/wysiwyg/products/2024/DES01655M/dimension_size_of_ESP32_C3_devlopment_board.webp

## License

The library files in this repository are released under the **CERN-OHL-S-2.0** license. See [LICENSE](LICENSE). Product names and trademarks belong to their respective owners. This is an independent community project and is not endorsed by Elecrow.
