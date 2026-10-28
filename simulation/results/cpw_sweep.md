# CPW 2D Pre-Check — JLC04161H-7628

This is the output of the 2D quasi-static pre-check. It is not a full-wave
result: use it to choose the starting W/S, and treat the 3D model and the
VNA coupon as the final checks.

## Nominal (dx = 0.01 mm)

| W (mm) | S (mm) | h (mm) | Z0 (Ω) | εeff | C_air (pF/m) | C_die (pF/m) |
|---:|---:|---:|---:|---:|---:|---:|
| 0.38 | 0.20 | 0.210 | 50.36 | 3.507 | 35.4 | 124.0 |

## Sweep (dx = 0.01 mm)

| W (mm) | S (mm) | Z0 (Ω) | εeff |
|---:|---:|---:|---:|
| 0.34 | 0.18 | 52.87 | 3.461 |
| 0.34 | 0.20 | 53.46 | 3.477 |
| 0.34 | 0.22 | 53.95 | 3.492 |
| 0.38 | 0.18 | 49.83 | 3.492 |
| 0.38 | 0.20 | 50.36 | 3.507 |
| 0.38 | 0.22 | 50.80 | 3.523 |
| 0.42 | 0.18 | 47.15 | 3.522 |
| 0.42 | 0.20 | 47.64 | 3.538 |
| 0.42 | 0.22 | 48.04 | 3.553 |

## Notes

- Target: 50 Ω ±5% (47.5–52.5 Ω).
- The 2D model ignores the 3D launch, the U.FL, the via fence, and finite
  copper thickness. Those are for the 3D model and the VNA coupon.
- Solder mask is included as a 0.01 mm layer with εr = 3.3.
- The prepreg is snapped to the grid; the 3D model uses the exact
  0.2104 mm stackup.
