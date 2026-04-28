# Papers

This repository collects compact working papers around **MELT** —
*Minimale Erhaltungs- und Landauer-Topologie* ("Minimal Conservation and
Landauer Topology"). MELT is a speculative information-geometry framework
built on a single norm: a **quantum-bit / energy correspondence**, in
which physical states carry an information content measured in bits and
the Landauer cost k_B·T·ln 2 per bit fixes the conversion to energy. Every
observable is read as a projection from this bit-energy ledger.

Two ingredients, no free parameters:

1. **Bit–energy norm.** Physical states have a discrete information
   content. Storing or erasing one bit has a thermodynamic cost
   (Landauer's principle). MELT promotes this from a metaphor to a
   bookkeeping rule: branching ratios are Shannon entropies of bit-erasure
   events, decay Q-values are Landauer heat, and observable energies are
   read as bit-counts times a unit cost.

2. **Born / off-diagonal split.** The modulus-squared readout (Born rule)
   keeps the diagonal of an underlying complex or Hermitian observable and
   erases a directed phase. MELT tries to make the lost phase explicit and
   recoverable from interferences and shape information that survive the
   projection — angular distributions, threshold steps, q²-shape, etc.

The notes here are exploratory working notes, not formal submissions. They
try to keep three layers separate:

- the published experimental or observational input,
- the standard operator or model language used by the field,
- the additional MELT interpretation proposed on top of that input.

## Papers

- [Paper_VectorThresholds](Paper_VectorThresholds/) — a compact MELT reading of
  LHCb arXiv:2603.12477, focusing on the vector-sector threshold at the
  open-charm `DD*` gate.

## Simulations

- [Blackhole-Eigenlight-Simulator (LRD)](Blackhole-Eigenlight-Simulator-LRD/) —
  a minified browser simulation for the LRD black-hole eigenlight picture, with
  helper overlays hidden by default. GitHub Pages:
  <https://georglegato.github.io/papers/>
