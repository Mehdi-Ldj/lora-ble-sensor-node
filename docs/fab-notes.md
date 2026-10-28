# Rev A fabrication notes

**Status:** Rev A is frozen and has not been ordered. The checks below are what
an order depends on.

## Order

- 4 layers, JLC04161H-7628, 1.6 mm nominal.
- 1 oz copper, outer and inner.
- Green solder mask, white silkscreen.
- ENIG finish, to confirm at order.
- IPC class 2, 100% electrical test, to confirm at order.
- Outline 55 mm × 55 mm.

## Design rules

| Rule | Value |
|---|---|
| Minimum track width | 0.20 mm |
| Minimum clearance | 0.15 mm |
| Minimum drill | 0.20 mm |
| Through vias | 0.30/0.20 mm and 0.20/0.20 mm |
| Blind/buried vias | none |
| Via tenting | front and back |
| Fiducials | FID1–FID3 |
| Mounting holes | H1–H3, 2.7 mm NPTH |

## Impedance

The RF nets are routed in the `RF_50R` net class. Targets, track geometry and
tolerance are in [`impedance.md`](impedance.md), and the layer heights they
depend on are in [`stackup.md`](stackup.md). JLC's impedance report or a coupon
measurement is still outstanding.

## In the release package

- Gerbers and the `.gbrjob` file (four copper layers, mask, paste, silkscreen,
  edge cuts)
- Excellon drill
- IPC-2581 netlist (`board.xml`)
- BOM (`bom.csv`, `jlc-bom.csv`)
- Placement (`cpl.csv`, `jlc-cpl.csv`)
- `manifest.sha256` and `README.txt`

Not produced by the release: ODB++, drill maps, board and stackup drawings, the
impedance report and the 3D STEP. The drawings and impedance report come from
JLC's order flow, so request them with the order rather than expecting them in
the archive.

## Notes

- Do not modify the 2.4 GHz antenna, the J6 keepout or the 868 MHz RF routing.
- Keep the bottom silkscreen table readable from the bottom.
- The exact vendor J6 STEP is not part of the release package.
