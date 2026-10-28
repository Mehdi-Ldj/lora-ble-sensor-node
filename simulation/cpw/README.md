# CPW pre-check and 3D plan

**Status:** the 2D quasi-static pre-check is complete. The 3D model is specified
but not run, and the VNA coupon is still the final check.

The 868 MHz and 2.4 GHz feeds use a grounded coplanar waveguide on the
JLC04161H-7628 stackup. This directory holds the pre-check, the 3D model
requirements and the acceptance criteria; the geometry itself is frozen in the
layout.

## The 2D pre-check

The pre-check is a 2D finite-volume quasi-static solve of the cross-section: it
computes the air and dielectric capacitances, then Z0 and εeff from the
quasi-TEM formulas.

Nominal geometry: W = 0.38 mm, S = 0.20 mm, h = 0.2104 mm, εr = 4.6, mask
0.01 mm at εr 3.3.

| Quantity | Result |
|---|---:|
| Z0 | 50.36 Ω |
| εeff | 3.51 |
| C_air | 35.37 pF/m |
| C_die | 124.05 pF/m |
| Guided λ at 868 MHz | 184 mm |
| Guided λ at 2.4 GHz | 66.7 mm |

Sweep at the same grid:

| W (mm) | S = 0.18 | S = 0.20 | S = 0.22 |
|---:|---:|---:|---:|
| 0.34 | 52.87 | 53.46 | 53.95 |
| 0.38 | 49.83 | **50.36** | 50.80 |
| 0.42 | 47.15 | 47.64 | 48.04 |

The line is width-dominated: W ±0.02 mm moves Z0 by about ∓2.2 Ω, while
S ±0.02 mm moves it by about ±0.5 Ω. With JLC's etch tolerance, 0.38/0.20 stays
inside 50 Ω ±5 % (47.5–52.5 Ω), so it is the starting geometry.

The 2D model ignores copper thickness, the launch, the via fence, finite ground
width and dispersion. Those are what the 3D model and the coupon are for.

## The 3D model

The 3D model has not been run yet. It has to include:

- L1 trace and top ground at 0.035 mm copper.
- Prepreg 0.2104 mm, εr 4.6, tanδ 0.02.
- L2 ground at 0.2104 mm below the trace.
- Solder mask 0.01 mm, εr 3.3.
- Via fence: 0.3 mm drill, 0.6 mm pad, 1.2 mm pitch.
- A 20 mm line, 2 mm ground width and an air box above.
- 50 Ω ports at both ends, with the port discontinuity de-embedded.
- A 0.1–3 GHz sweep.

On ports: prefer a waveguide port with the CPW mode and an integration line from
the trace to the ground. If the tool cannot express a CPW mode, use a 50 Ω lumped
port at each end and de-embed a short feed line. A wrong port is the usual cause
of a wrong S11, so check it against a matched thru.

On boundaries and mesh: radiation or PML on the top and sides, electric at the
L2 ground; about 0.05 mm at the 0.20 mm gap and 0.1–0.2 mm elsewhere, with
adaptive refinement until Z0 and S11 stop moving.

Post-processing: S11 and S21, Z0 from the port or TDR, εeff from the S21 phase,
current density on the via fence, and a Touchstone `.s2p`.

## Acceptance

| Check | Target |
|---|---|
| Z0 | 50 Ω ±5 % (47.5–52.5 Ω) |
| S11, line and launch | ≤ −15 dB, target −20 dB |
| S21 at 868 MHz | consistent with a 20 mm line |
| S21 at 2.4 GHz | no via-fence resonance |
| 2D against 3D | within about 5 Ω |
| Coupon against simulation | within about 5 Ω |

## VNA coupon

A 30 mm CPW coupon on the same panel and stackup, with the same launch and
finish:

- SOLT calibration.
- S11/S21 with the launches de-embedded.
- Z0 extracted from the coupon and compared with the 3D model.
- If the coupon is off by more than 5 Ω, tune W first and S second, then rerun
  the model before changing the layout.

## Next steps

1. Run the 3D model.
2. Compare Z0 and S11 against the 2D pre-check (50.36 Ω, εeff 3.51).
3. If Z0 falls outside 47.5–52.5 Ω, move W by ±0.02 mm and rerun.
4. Add the coupon and its test points to the next revision of the board.
