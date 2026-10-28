# Rev A PCBA notes

**Status:** Rev A is frozen. The part and DFM checks below were made before the
freeze; stock and lead times have to be re-checked at order time.

## Part availability and assembly flags

| Part | LCSC | Package | JLCPCB assembly | Notes |
|---|---|---|---|---|
| nRF52840-QIAA-R | C190794 | AQFN-73-EP 7×7 | Extended; Economic & Standard | MSL 3; X-ray required |
| SX1262IMLTRT | C191341 | QFN-24-EP 4×4 | Extended; Economic & Standard | MSL 1 |
| BQ25570RGRR | C506250 | VQFN-20-EP 3.5×3.5 | Extended; Economic & Standard | Stock is low (hundreds); pre-order or consign |
| BME280 | C92489 | LGA-8 2.5×2.5 | Extended; Standard only | High difficulty; X-ray required |

## What the part choices force

- Standard PCBA, not Economic, because the BME280 is Standard-only.
- X-ray inspection for the aQFN73 and the BME280; it has to be in the quote.
- All four ICs are extended parts, so expect extended-part fees.
- BQ25570 stock is low. Pre-order it, consign from Digi-Key or Mouser, or move
  to a BQ25504 with an external boost or an SPV1050 and re-check the power tree.
- The BQ25570 has no battery temperature detection. An NTC and an
  MCU-controlled charge inhibit cover the 0–45 °C window.
- JLCPCB's PCB minimum is five, so assemble two to five boards.
- Three global fiducials are on the board, along with the mounting holes for
  tooling; CPL rotations still have to be checked at order time.

## Before ordering

1. Re-check JLCPCB stock for every part.
2. Pre-order the BQ25570 and a spare, or choose the alternative.
3. Confirm the Standard PCBA and X-ray quote.
4. Check the aQFN73 and BME280 footprints and paste against JLCPCB/EasyEDA data.
5. Regenerate the BOM and CPL in JLCPCB format and check rotations against the
   assembly drawing.


