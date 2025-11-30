# Blazar Hadronic (pγ) Model — Markdown Script

This markdown script is derived from the README and formatted for easy reference, publication, or documentation.

---

## Overview

This project implements a **hadronic (pγ) blazar emission model** capable of simulating:

* Proton injection
* pγ interaction efficiency
* Neutrino and gamma-ray production
* Time-dependent flare behavior
* Expected gamma-ray counts for a VERITAS-like instrument

---

## Features

### Proton Injection

* Power-law proton spectrum with an exponential cutoff
* Normalization computed to match a specified proton luminosity

### pγ Interaction

* Parameterized energy-dependent efficiency
* Inelasticity factor describing pion energy fraction

### Particle Production

* Charged pion → neutrinos
* Neutral pion → gamma rays
* Simple energy-fraction mapping (0.05 for neutrinos, 0.1 for gamma rays)

### Flare Simulation

* Gaussian-shaped flare profile
* Adjustable width and center
* Integrated flux across an observing window

### Instrument Response

* Placeholder VERITAS-like effective area function
* Computation of expected gamma-ray counts

---

## Dependencies

Install the required packages using:

```bash
pip install numpy scipy matplotlib astropy
```

---

## Running the Script

Run the model using:

```bash
python blazar_hadronic_model.ipynb
```

Outputs include:

* Neutrino and gamma-ray differential spectra
* Effective area curve
* Flare time evolution
* Expected gamma counts for a given observing window

---

## Code Components

### Proton Spectrum

* Power law with exponential cutoff
* Normalization ensures total proton luminosity matches input

### pγ Efficiency

* ( f_{p\gamma}(E) = f_0 (E/E_0)^\beta )
* Capped at 1.0

### Mapping to Secondary Particles

* Neutrino production uses charged-pion fraction
* Gamma-ray production uses neutral-pion fraction

### Flux Calculation

* Converts luminosity → flux via luminosity distance
* Outputs both differential number flux and energy flux

---

## Plotting

The script automatically produces:

1. Neutrino and gamma-ray spectra
2. Effective area vs energy
3. Time-dependent flare curve

---

## Notes

* This model is pedagogical, not physically complete
* Energy mapping uses simple fractions, not full kinematic modeling
* VERITAS response curve is purely a placeholder
* Cosmology approximation is valid only for small redshift

---

## License

Free to use, modify, and share. Attribution is appreciated.
