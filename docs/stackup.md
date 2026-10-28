# Rev A stackup

Source: KiCad board stackup for `hardware/rev-a/lora-node.kicad_pcb`  
Order stackup: **JLC04161H-7628**

| Layer        | Material                        |     Thickness |
| ------------ | ------------------------------- | ------------: |
| F.Mask       | green solder mask               |      0.010 mm |
| F.Cu         | copper, 1 oz                    |      0.035 mm |
| Dielectric 1 | FR4 prepreg, Er 4.6, tan δ 0.02 |     0.2104 mm |
| In1.Cu       | copper, 1 oz                    |      0.035 mm |
| Dielectric 2 | FR4 core, Er 4.6, tan δ 0.02    |      1.040 mm |
| In2.Cu       | copper, 1 oz                    |      0.035 mm |
| Dielectric 3 | FR4 prepreg, Er 4.6, tan δ 0.02 |     0.2104 mm |
| B.Cu         | copper, 1 oz                    |      0.035 mm |
| B.Mask       | green solder mask               |      0.010 mm |
| **Total**    |                                 | **1.6208 mm** |

The KiCad total includes both solder-mask layers. The JLC order thickness is
**1.6 mm nominal**.

## Fabrication rules

- 4 layers, 1 oz copper.
- Minimum track width: 0.20 mm.
- Minimum clearance: 0.15 mm.
- Minimum drill: 0.20 mm.
- Through vias: 0.30/0.20 mm and 0.20/0.20 mm; no blind or buried vias.
- Via tenting: front and back.
- Solder mask: green; silkscreen: white.
- Surface finish: ENIG, to confirm at order.
- Board outline: 55.0025 mm × 55.0025 mm.
- Fiducials: FID1–FID3.
- Mounting holes: H1–H3, 2.7 mm NPTH.

## Impedance

The RF nets are routed in the `RF_50R` net class; the target, trace geometry and
tolerance are in [`impedance.md`](impedance.md). JLC's impedance report is still
outstanding.
