# M-IP Slag Viscosity Model

Python simulation of high-temperature slag viscosity, based on the Modified
Inclined Plane (M-IP) method from:

Dai, B., Wu, X., & Zhang, L. (2018). Fuel, 233, 299-308.

Extended with transient heating and friction for a specific lab furnace
setup, under guidance from Prof. Ashok Kamaraj.

## Contents

- Part 1 (Cells 1-5): reproduces the paper's own flow equation directly
- Part 2 (Cells 6-12): adds heating time, temperature-dependent viscosity,
  and friction, solved together over time for each of the seven ash samples

## Status

**First draft.** Runs end to end and produces physically consistent results,
but is not yet calibrated against real lab measurements.

## Placeholders

Values below are estimates, not measurements. Each needs real data before
results can be trusted quantitatively.

**Bulk density (rho)** — molten slag density, currently a general textbook
estimate. Needs a real value for this specific ash composition.

**Film thickness (delta)** — set within the paper's reported range
(<0.1mm), not measured directly for this setup.

**Per-ash melting threshold (T_melt)** — guessed temperatures, ordered by
silica content. Needs real ash-fusion-temperature data or direct observation.

**Convective heat transfer coefficient (h_conv)** — depends on furnace gas
flow rate and geometry, currently a generic estimate.

**Emissivity** — within the standard range for oxide surfaces, not measured
for this specific ash.

**Specific heat (cp)** — same value shared across all seven ashes, based on
published blast-furnace-slag data rather than this composition.

**Friction coefficient (mu_friction)** — slag-on-corundum friction, not
measured. Needs an experimental estimate.

**Arrhenius calibration (A_A, E_A)** — only one real data point exists per
ash (viscosity at 1400C). A second real measured point per ash is needed
for a proper two-point fit.
