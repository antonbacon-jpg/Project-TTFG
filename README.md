# Toroidal Time Field Gravity (TTFG)

A GR-inspired alternative to dark matter for galaxy rotation curves.

**Author:** Anton Bacon, with AI-assisted mathematical verification by Claude (Anthropic) — Sonnet 4.6, March 2026.

## What this is

Toroidal Time Field Gravity (TTFG) explains galaxy rotation curves without invoking dark matter. The central mechanism is GR frame-dragging of disk angular momentum producing a toroidal time field whose velocity profile follows the Lamb-Oseen vortex equation.

A single set of 24 global parameters applies to all 193 galaxies. There are no per-galaxy free parameters of any kind — not for stellar mass, dark matter halos, or rotation curve shape. All 24 parameters describe the toroidal field physics.

## Results (as reported in the paper)

Tested on 193 galaxies from the SPARC and LITTLE THINGS datasets:

- Beats Modified Newtonian Dynamics (MOND) on 148 of 193 galaxies (76.7%)
- Mean RMSE: 15.03 km/s vs MOND's 30.59 km/s (51% reduction)
- LITTLE THINGS dwarf irregulars: 13/13, mean 8.18 vs MOND 34.1 km/s
- Four-stage toroidal collapse sequence (Spearman r = +0.852, p < 0.0001), predicting 13 pre-AGN candidates testable by radio/X-ray observation
- Specific quantitative predictions for nuclear magnetic field strengths in five AGN galaxies

## Honest limitations

- In-sample fit: the 24 parameters were fitted on the same 193 galaxies they are evaluated on. No held-out / cross-validation is described in the paper. The next step is proper train/test split and out-of-sample validation.
- The MOND comparison in the paper uses fixed stellar mass-to-light ratio Υ★ = 1.0. Standard MOND fits Υ★ per galaxy. A fair comparison needs MOND with per-galaxy fitted Υ★, plus NFW, on the same held-out protocol.
- The frame-dragging magnitude step (G_t = c × L_t) is an empirical scaling, not a derivation from Einstein's equations at the claimed magnitude. Presented here as an empirical vortex model inspired by the frame-dragging analogy.
- Five AGN galaxies use estimated, not measured, nuclear magnetic field (BGI) values. Those are predictions, not inputs.

## Reproduction

- Full model code (TTFG_model.py, SC27) is included in Section 4 of the paper PDF.
- Data: SPARC (Spitzer Photometry and Accurate Rotation Curves) + LITTLE THINGS rotation-curve files. The paper's master table and optimizer are not in this repo — the PDF is the self-contained record.
- The author's workflow: local Python runs on SPARC data, readout pasted to Claude for analysis, variables added iteratively, re-test. Claude coded to spec; the author ran, decided, and verified.

## Files

- `Toroidal_Time_Field_Gravity_Bacon_Claude_2026_redacted.pdf` — Full paper, with contact email redacted. 29 pages.

## Citation

Bacon, A. (2026). Toroidal Time Field Gravity: A GR-Derived Alternative to Dark Matter for Galaxy Rotation Curves. With AI-assisted mathematical verification by Claude (Anthropic) — Sonnet 4.6.
