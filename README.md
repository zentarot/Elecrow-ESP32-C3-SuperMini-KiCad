# Elecrow ESP32-C3 SuperMini — KiCad Library

Unofficial KiCad symbol and through-hole footprint library for the **Elecrow ESP32-C3 SuperMini development board**.

The **2.00 mm footprint variant has been physically validated by the repository maintainer**: a PCB was fabricated using this footprint and the module pin spacing/alignment matched. The 2.54 mm variant is retained as an alternative and is not the validated default.

![Elecrow ESP32-C3 SuperMini module](images/esp32-c3-supermini.jpg)

## Included

- `ESP32-C3-SuperMini_Elecrow.kicad_sym` — schematic symbol with 16 named pins and electrical connection endpoints. Its default footprint field selects the validated 2 mm variant.
- `ESP32-C3-SuperMini_Elecrow.pretty/` — two footprint variants:
  - **`ESP32-C3-SuperMini_Elecrow_2mm` — recommended / physically validated.**
  - `ESP32-C3-SuperMini_Elecrow_2.54mm` — alternative standard-pitch variant; verify before use.
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
4. The symbol's default footprint points to `ESP32-C3-SuperMini_Elecrow:ESP32-C3-SuperMini_Elecrow_2mm`. Keep this selection for the validated variant.

### Footprint library

1. Copy the `ESP32-C3-SuperMini_Elecrow.pretty` directory to a stable location.
2. In **Preferences → Manage Footprint Libraries**, add it as a project-specific or global library.
3. Use the library nickname `ESP32-C3-SuperMini_Elecrow`, or update the symbol's footprint field to match your chosen nickname.
4. Select `ESP32-C3-SuperMini_Elecrow_2mm` for the physically validated footprint. The 2.54 mm alternative is provided separately.

The included `fp-lib-table` is an example; edit its path if you use it.

## Dimensions and fabrication notes

The validated 2 mm variant uses a 2.00 mm adjacent-pad pitch and 18.00 mm row-center spacing. The alternative 2.54 mm variant uses a 2.54 mm adjacent-pad pitch and 18.60 mm row-center spacing. Both footprints currently use a 21.6 × 25.2 mm board outline, 1.8 mm circular through-hole pads, and 1.0 mm drills.

Physical validation applies to the board revision used for the maintainer's fabrication test. ESP32-C3 SuperMini-compatible boards from other suppliers or revisions may differ. Before using this footprint with a different module revision, check pad alignment, module outline, USB connector clearance, and pin mapping. Run KiCad design-rule checks for your own PCB.

This is an independent community project, not an official Elecrow design file, and is not endorsed by Elecrow. Use the files at your own risk.

## Reference material

- Elecrow pin definition: https://media-cdn.elecrow.com/media/webp_image/wysiwyg/products/2024/DES01655M/pin_definition_of_ESP32_C3_dev_board.webp
- Elecrow dimension drawing: https://media-cdn.elecrow.com/media/webp_image/wysiwyg/products/2024/DES01655M/dimension_size_of_ESP32_C3_devlopment_board.webp

## License

Released under the MIT License. See [LICENSE](LICENSE). Product names and trademarks belong to their respective owners.
