# Rev A assembly notes

**Status:** Rev A is frozen and has not been ordered. The checks below are what
an order depends on.

## Assembly side

- Top side only.
- No SMD components are on the bottom side.
- The bottom silkscreen is a reference table for connectors and test points.

## JLC SMT

The JLC SMT BOM/CPL include all populated SMD references, including:

- C32 and C33 (100 nF, 0402)
- J6 (Murata MM8130-2600 coax switch)

J6 still has to be checked against the JLC/LCSC assembly library before
ordering. Its LCSC part is `MM8130-2600RB8`; the exact vendor model is the same
connector in a different reel package (`RA2` vs `RB8`).

## JLC THT

The following through-hole parts are included in the JLC THT assembly BOM/CPL:

| Ref | Part | Function |
|---|---|---|
| J1 | JST PH 2-pin, `B2B-PH-K-S` | solar input |
| J2 | JST PH 2-pin, `B2B-PH-K-S` | LiFePO4 battery |
| J4 | JST PH 3-pin, `B3B-PH-K-S` | soil probe |
| TH1 | JST XH 2-pin, `B2B-XH-A` | external 10 kΩ NTC on the battery |
| JP1 | 2.54 mm 1×2 header, `PZ254V-11-02P` | battery measurement, `FIT SHUNT` |

JP1 is the battery-measurement connector. It is not a DNP part and is not
hand-fit in the release definition.

## Population

- No DNP parts in the release BOM.
- All BOM references are populated.
- Test points, fiducials and mounting holes are not BOM/CPL items.

## Assembly drawing

The top assembly drawing must show:

- all references and values;
- pin 1 and polarity;
- connector orientation and pinouts;
- the antenna keepout;
- the JP1 `FIT SHUNT` marking;
- the SMD versus THT assembly split.

The bottom drawing is for reference and inspection only.

## Checks before ordering

- JLC SMT and THT BOM/CPL reference sets match the release BOM.
- Every CPL rotation is checked against the assembly drawing and JLC preview.
- Last JLC lookup: 96/96 refs found, all in stock, 10 Basic and 48 Extended.
- No DNP part appears in the JLC BOM or CPL.
