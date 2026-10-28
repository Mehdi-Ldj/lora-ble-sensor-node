# Rev A controlled impedance

**Status:** design value. JLC's impedance report is still outstanding, and
nothing here has been measured.

## RF net

| Item | Value |
|---|---|
| Net class | `RF_50R` |
| Target | 50 Ω single-ended |
| Tolerance | ±10% |
| Track width | 0.38 mm |
| Reference plane | In1.Cu |
| Stackup | JLC04161H-7628 |
| Dielectric below trace | 0.2104 mm prepreg |

The 2.4 GHz antenna feed, J6 path and 868 MHz RF path are routed in the
`RF_50R` net class. Do not change the trace width, reference plane or antenna
keepout without re-running the impedance calculation and JLC DFM review.

## Before ordering

JLC's impedance report or a test-coupon result has to be attached and the
fabricated stackup confirmed. The target above is a design value, not a
measurement.
