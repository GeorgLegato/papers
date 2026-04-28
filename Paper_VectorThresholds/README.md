# Vector Thresholds as a MELT Ledger

## A compact reading of LHCb arXiv:2603.12477

**Status:** working note / MELT Rechenbeispiel, April 2026.
Loose public deployment, no formal submission.
**Primary paper read here:** LHCb arXiv:2603.12477 (LHCb-PAPER-2025-055).
**Public LHCb dataset used for diagnostics:** Zenodo DOI `10.5281/zenodo.19497184`
(LHCb's own data release, not this note).

### Abstract

LHCb's 2026 amplitude analysis of $B^+\to K^+\mu^+\mu^-$ is not a
classic angular-observable paper. It is an unbinned amplitude analysis of the
dimuon mass spectrum over $300<m_{\mu\mu}<4700\,\mathrm{MeV}/c^2$, with
local Wilson coefficients and nonlocal charm/light resonances fitted in one
model. In the published interpretation the result is a familiar vector-sector
deficit: the preferred effective coefficient $C_V=C_9+C_9'$ is below its
Standard Model value, with the stated tension depending strongly on the
chosen lattice-QCD form factors.

This note asks a narrower question: how does the result look when read through
the local MELT bookkeeping rules? Two robust structures and one suggestive
mass coincidence stand out. First, the two-dimensional likelihood in
$(C_V,C_A)$ is annular because the short-distance branching fraction
constrains mainly $C_V^2+C_A^2$; this is the observable shape expected from a
Born-style modulus readout, and is a structural prediction independent of any
fit. Second, the paper reports a step-like vector response at the open-charm
$DD^{\ast}$ threshold, $\Delta_{DD^{\ast}}=-1.37\pm0.53$, while a simple binned
count model does not see a standalone bump; the effect lives in the
operator/amplitude ledger rather than in raw event counts.

The third element is a threshold arithmetic that is unusually sharp:

$$
m_{DD^{\ast}}-m_{J/\psi}=775.05\,\mathrm{MeV},\qquad
m_{\rho}=775.26\,\mathrm{MeV},
$$

i.e. the open-charm threshold sits one $\rho(770)$ quantum above $J/\psi$. We
note that this near-coincidence has an established physical anchor: the
exotic state $X(3872)$ has $m=3871.64\pm0.06\,\mathrm{MeV}$, matching
$m_{DD^{\ast}}=3871.69\,\mathrm{MeV}$ within PDG precision, and $X(3872)\to
J/\psi\,\rho$ is a documented decay channel. The MELT reading is that the
reported vector gate at $DD^{\ast}$ opens exactly at the $J/\psi+\rho$
mode-lock realised physically by the $X(3872)$, at the CP³ hadron-bus to CP⁴
domain-wall transition.

![MELT map for the LHCb threshold ledger](figures/fig1-lhcb-melt-ledger.svg)

*Figure 1. Minimal map used in this note. LHCb provides the mass-spectrum
amplitude fit; MELT reads its annulus, vector threshold, and axial drift as a
CP³/CP⁴ ledger rather than as a new raw resonance peak.*

## 1. What LHCb Actually Measured

The LHCb paper studies $B^+\to K^+\mu^+\mu^-$ using an effective Hamiltonian
with Wilson coefficients $C_i$ multiplying local operators $O_i$. Heavy
degrees of freedom are integrated out; what remains is a set of operator
channels whose coefficients are inferred from data. The local combinations of
interest are

$$
C_V = C_9 + C_9',\qquad C_A = C_{10}+C_{10}'.
$$

The analysis uses the full reconstructed dimuon mass range and includes
one-particle and two-particle nonlocal amplitudes. The Zenodo release gives
the selected unbinned dimuon masses, plus the background line shape, background
fraction, efficiency curves, and resolution functions needed to reproduce the
published mass-spectrum analysis at the support-curve level.

The headline numbers used in this note are:

| Quantity | Paper-level value used here | Role |
|---|---:|---|
| $C_V^\mathrm{SM}$ | $4.273$ | SM vector anchor |
| $C_A^\mathrm{SM}$ | $-4.166$ | SM axial anchor |
| $C_V^\mathrm{fit}$ | $\approx 3.4 \pm 0.2$ | best-fit vector value, read from Fig. 4 |
| $C_A^\mathrm{fit}$ | $\approx -3.0 \pm 0.2$ | best-fit axial value, read from Fig. 4 |
| $C_A(q^2)$ slope | $b=-0.090\pm0.045$ | residual scale drift, $\sim 2\sigma$ |
| $C_V$ step at $DD^{\ast}$ | $\Delta_{DD^{\ast}}=-1.37\pm0.53$ | threshold response, $\sim 2.6\sigma$ |

LHCb quotes $\Delta_{DD^{\ast}}$, $\Delta_{J/\psi}=0.41\pm0.24$, and the
$C_A(q^2)$ slope as explicit numerical results. The absolute best-fit
$(C_V,C_A)$ are not given as scalars in the paper text; we read them from the
2D likelihood surface in Fig. 4 with an estimated reading uncertainty of
$\pm 0.2$. That uncertainty propagates into every comparison below; we mark
where it bites.

The reported Standard Model tension is not a single invariant headline. With
HPQCD form factors LHCb quotes about $4.0\sigma$; with FNAL/MILC form factors
the same analysis gives about $1.6\sigma$. That dependence matters. In this
note the form-factor dependence is treated as a guardrail: the robust object is
not "new particle found", but the pattern of how the vector and axial ledgers
move when the nonlocal charm model is included.

## 2. MELT Basics Needed Here

Four pieces of MELT bookkeeping are needed for this note.

### 2.1 Born Readout

MELT distinguishes a pre-readout complex or hermitian ledger from the scalar
quantity observed after Born projection. For a complex amplitude $u=a+bi$ the
Born readout keeps

$$
u\bar u=a^2+b^2,
$$

while the holomorphic square

$$
u^2=(a^2-b^2)+2ab\,i
$$

keeps a directed off-diagonal phase. The claim is not that Born's rule fails
as a measurement prescription. The claim is that a modulus-squared readout is
incomplete as geometry because it removes the directed phase.

This is why an annular likelihood matters. If a fit primarily constrains
$C_V^2+C_A^2$, it is reading a radius in coefficient space. Orientation is
then recovered only through interference with nonlocal amplitudes. That is the
same pattern as: norm first, phase later.

### 2.2 CP³/CP⁴/CP⁵ Bridge

In the local MELT inventory the bridge between hadronic and lepton/vector
readout is the classical band

$$
\mathrm{CP}^3+\mathrm{CP}^4+\mathrm{CP}^5 = 28+0+4 = 32\ \mathrm{bit}.
$$

The roles are:

| CP block | MELT role | Meaning in this note |
|---|---|---|
| CP³ | 28-bit hadron bus | charm/hadron channel enters |
| CP⁴ | 0-bit domain wall | transient threshold, no stable storage |
| CP⁵ | 4-bit lepton/vector bus | $\mu^+\mu^-$ readout exits |

The decay $B^+\to K^+\mu^+\mu^-$ is therefore a good test surface: it starts
in a hadronic transition, exits through a lepton pair, and is modeled by
Wilson coefficients that separate vector and axial operator channels.

### 2.3 Ballast Bit

A recurring MELT anchor is the first-split Shannon entropy of $K_S\to\pi\pi$,
$H_1=0.8901$ bit, which appears as a "ballast" value across several
hadron/lepton splits. We do not use it as proof. We use it only as a scale
check on the vector deficit:

$$
\Delta C_V = C_V^\mathrm{SM}-C_V^\mathrm{fit}
\approx 4.273-3.4 = 0.87 \pm 0.2,
$$

so

$$
\frac{\Delta C_V}{0.8901}\approx 0.98 \pm 0.2.
$$

The ratio is consistent with one within the reading uncertainty on
$C_V^\mathrm{fit}$, but it is not a discriminating test on its own. Reducing
the reading uncertainty (either from a likelihood-table extraction or from a
local refit of the unbinned data) is required before this comparison can be
promoted from "scale check" to "quantitative claim." The structural arguments
of this note do not depend on it.

### 2.4 The rate-only diagonal projection

The Born-readout language of §2.1 has a concrete operational form in this
analysis, but not via an angular $V$–$A$ interference. In $B\to K$ (two
pseudoscalars), the hadronic side admits no axial-vector form factor; the
lepton-side $V$ and $A$ pieces enter the squared amplitude as
**independent moduli, with no rate-level cross-term**. The differential
rate (Eq. 19 of arXiv:2603.12477) is

$$
\frac{d^2\Gamma_\mu}{dq^2\,d\cos\theta_\ell}\;\propto\;
|k|^2\beta_+^2(1-\cos^2\theta_\ell)\,|C_A|^2\,f_+^2
\;+\;\frac{m_\mu^2(M_B^2-M_K^2)^2}{q^2\,M_B^2}\,|C_A|^2\,f_0^2
\;+\;|k|^2(1-\beta_+^2\cos^2\theta_\ell)\,|C_V^{\mathrm{eff}}\,f_+ +
2(C_7^{\mathrm{eff}}+C_7')\tfrac{m_b+m_s}{M_B+M_K}\,f_T|^2,
$$

with **no term linear in $\cos\theta_\ell$**. The LHCb paper notes this
explicitly: a $\cos\theta_\ell$-linear (forward-backward-asymmetry-like)
term would require scalar, pseudoscalar, or tensor Wilson coefficients
that this analysis does not include. The reason is hadronic: between two
pseudoscalars the $V$–$A$ interference contracts with a symmetric
hadronic tensor and vanishes by Lorentz structure.

Integrating over $\cos\theta_\ell$ produces the $q^2$-only spectrum used in
the fit, schematically

$$
\frac{d\Gamma_\mu}{dq^2}\;\propto\;a(q^2)\,|C_A|^2\;+\;b(q^2)\,|C_V^{\mathrm{eff}}|^2,
$$

with $C_V^{\mathrm{eff}}=C_V+(\text{q}^2\text{-dependent nonlocal and }C_7\text{ pieces})$.
**There is no $V$–$A$ cross-term in the rate-only fit.** The annular shape
of the $(C_V,C_A)$ likelihood is the iso-rate contour of

$$
a\,|C_V|^2 + b\,|C_A|^2\;\approx\;\mathrm{const},
$$

which after $q^2$-integration has $\langle a\rangle$ and $\langle b\rangle$
of the same order, giving an approximate circle. In MELT-Born language: the
rate-only fit reads two independent moduli; the relative phase between $C_V$
and $C_A$ does not enter.

What recovers $C_V$ vs $C_A$ direction is **not** an angular variable —
there is none in this decay — but the $m_{\mu\mu}$-spectrum *shape*. The
nonlocal amplitudes $Y_{c\bar c}(q^2)$ (charm loops, $\psi$ resonances) and
$Y_\mathrm{light}(q^2)$ ($\rho/\omega/\phi$) inside $C_V^\mathrm{eff}$ carry
nontrivial $q^2$-dependent phases. $C_V$ interferes with these complex
amplitudes in a way that depends on $m_{\mu\mu}$, and the fit picks up the
orientation in $(C_V,C_A)$-space from how this interference shapes the
spectrum. This is what the LHCb paper means by "the fit distinguishes
between $C_V$ and $C_A$ through the interference of $C_V$ with the nonlocal
amplitudes." The Born-readout reading is correct in spirit — *modulus from
the rate, phase from elsewhere* — but the "elsewhere" here is the
$m_{\mu\mu}$-shape via nonlocal-amplitude interference, not a $\cos\theta_\ell$
angular variable.

A note on $B^0\to K^{\ast 0}\mu^+\mu^-$ angular analyses ($P_5'$,
$A_\mathrm{FB}$, $F_L$, $S_3$, …): the $K^{\ast}$ is a vector meson, so the
hadronic tensor has seven form factors and the amplitude decomposes into
transversity amplitudes ($A_\perp$, $A_\parallel$, $A_0$). Wilson
coefficients enter those transversity amplitudes in richer combinations
than they do in the $B\to K$ rate, and the angular asymmetries probe
Wilson information not visible here. We mention this only as an indication
that the Wilson-coefficient ledger is fuller than what the $B^+\to K^+\mu\mu$
rate-only annulus shows; we do not claim that the $K^{\ast}$ angular
observables are a direct readout of a single $\mathrm{Re}(C_V^{\ast}C_A)$
matrix element.

A consequence for this note: the annulus of Fig. 4 is the unavoidable shape
of any rate-only fit over $(C_V,C_A)$ when the two enter as independent
moduli with comparable kinematic weights. It is not diagnostic of new
physics. The diagnostic content sits elsewhere — in the radius (overall
Wilson-coefficient deficit), in the threshold step ($X(3872)$-like nonlocal
structure), and in the $C_A(q^2)$ drift.

## 3. The LHCb Result as a MELT Ledger

The working map is:

| LHCb object | Operator reading | MELT reading | Status |
|---|---|---|---|
| annular $(C_V,C_A)$ likelihood | rate fixes $C_V^2+C_A^2$ | Born-like modulus readout | structural, pre-data |
| $DD^{\ast}$ step in $C_V$ | vector threshold response | CP³→CP⁴ channel opens | empirical, $2.6\sigma$ |
| $C_A(q^2)$ slope | axial coefficient not fully local | incomplete coarse-graining | empirical, $2\sigma$ |
| $DD^{\ast}-J/\psi\simeq\rho$ | $X(3872)$ at threshold | mode-lock explains vector selection | known physics, MELT framing |
| $\Delta C_V \approx 0.873$ | vector coefficient deficit | $\approx 1$ ballast bit missing | scale check, not test |

The annular part is the conceptual lead, and §2.4 fixes the mechanism: the
rate-only short-distance constraint is the iso-contour of $a(q^2)|C_V|^2 +
b(q^2)|C_A|^2$, integrated over $q^2$ with comparable weights. $V$ and $A$
enter as independent moduli; there is no rate-level $V$–$A$ cross-term in
$B\to K\mu\mu$. The orientation in $(C_V,C_A)$-space is recovered from
$m_{\mu\mu}$-shape interference of $C_V$ with the complex nonlocal
amplitudes (the $C_V^\mathrm{eff}$ structure). **This argument does not
depend on a fitted number;** an annulus appears in any rate-only
$B^+\to K^+\ell^+\ell^-$ constraint where $V$ and $A$ have similar
integrated kinematic weights. It is the unavoidable shape of two
independent moduli with comparable coefficients, not a fit choice.

For scale, the SM and fit radii in coefficient space are

$$
R_\mathrm{SM}=\sqrt{C_V^2+C_A^2}\big|_\mathrm{SM}
=\sqrt{4.273^2+4.166^2}=5.968,
$$

$$
R_\mathrm{fit}\approx\sqrt{3.4^2+3.0^2}\approx 4.5 \pm 0.2.
$$

The radial deficit $\Delta R\approx 1.4 \pm 0.3$ is of the same order as
the reported step amplitude $|\Delta_{DD^{\ast}}|=1.37\pm 0.53$. We note
this scale match but do not claim it as a structural identity: $\Delta R$ is
a global 2D-radius shift while $\Delta_{DD^{\ast}}$ is a localised step in
$C_V$ at one threshold, and there is no a-priori reason for them to coincide
unless the threshold gate absorbs the entire radial shrinkage. That would be
a further claim, not implied by the present data.

## 4. The DD* Gate, the Rho Mode Lock, and the X(3872) Anchor

### 4.1 Mass arithmetic

The compact observation is pure mass arithmetic:

$$
m_{DD^{\ast}}=3871.70\,\mathrm{MeV},\qquad
m_{J/\psi}=3096.65\,\mathrm{MeV},\qquad
m_{DD^{\ast}}-m_{J/\psi}=775.05\,\mathrm{MeV}.
$$

The $\rho(770)$ mass is $m_\rho=775.26\,\mathrm{MeV}$, so

$$
(m_{DD^{\ast}}-m_{J/\psi})-m_\rho=-0.21\,\mathrm{MeV},
$$

a relative residual of $2.7\times10^{-4}$.

### 4.2 The X(3872) physical anchor

This near-coincidence is not unprecedented. The exotic state $X(3872)$, also
known as $\chi_{c1}(3872)$, has $J^{PC}=1^{++}$ and PDG mass

$$
m_{X(3872)}=3871.64\pm0.06\,\mathrm{MeV},
$$

i.e. it sits within $0.05\,\mathrm{MeV}$ of $m_{DD^{\ast}}$. A
well-established decay channel is $X(3872)\to J/\psi\,\rho^0\to
J/\psi\,\pi^+\pi^-$. The $X(3872)$ is therefore a physically realised
$DD^{\ast}\,$/$\,J/\psi\,\rho$ admixture sitting at the exact mass where
LHCb reports the vector-sector step. The "mode lock" between $J/\psi$ and
$\rho$ is not a MELT-introduced concept; it is a measured spectroscopic
feature of charmonium, and the MELT reading is that the $C_V$ step in this
channel is a manifestation of that admixture in the Wilson-coefficient
ledger.

### 4.3 Cross-channel specificity check

If the $J/\psi+\rho$ structure were a generic light-vector lock, analogous
threshold-resonance differences should reproduce other well-known light
vectors $\omega(782)$ or $\phi(1020)$. Direct check:

| Difference | Value (MeV) | Light vector candidate | Match? |
|---|---:|---:|---|
| $m_{DD^{\ast}}-m_{J/\psi}$ | $775.05$ | $m_\rho=775.26$ | $-0.21\,\mathrm{MeV}$ ✓ |
| $m_{DD}-m_{\eta_c}$ | $745.78$ | $m_\rho=775.26$ | $-29.5\,\mathrm{MeV}$ × |
| $m_{D^{\ast}D^{\ast}}-m_{\psi(2S)}$ | $327.60$ | none in $700{-}800$ band | × |
| $m_{D^{\ast}D^{\ast}}-m_{\psi(3770)}$ | $240.00$ | none | × |

Only the $J/\psi+\rho$ row matches at the $0.03\%$ level. The other
threshold-charmonium differences fall in regions with no similarly close
light-vector partner. This rules out the trivial reading "any threshold sits
one light-vector quantum above some charmonium" and supports the specific
$X(3872)$-mediated coupling reading: the lock is between $J/\psi$ and $\rho$,
not between any threshold and any vector.

### 4.4 Scalar null test

A separate falsification check: if the gate were generically light-meson
mediated (not specifically vector), an analogous scalar-meson difference
should also align. The closest scalar test is

$$
m_{DD^{\ast}}-m_{\eta_c}=3871.70-2983.90=887.80\,\mathrm{MeV},
$$

which falls $\approx 100\,\mathrm{MeV}$ below the broad $f_0(980)$ and has
no nearby narrow scalar. By the same precision standard that makes the $\rho$
match notable ($0.21\,\mathrm{MeV}$ residual), this scalar test fails by
two orders of magnitude. The threshold gate is specifically vector-selecting,
consistent with LHCb's report that the threshold step appears in $C_V$ and
not in a scalar/tensor channel.

### 4.5 Repeated spin gap (noted, not claimed)

For completeness, the charm-ladder mass differences

$$
m_{DD^{\ast}}-m_{DD}=142.02\,\mathrm{MeV},\qquad
m_{D^{\ast}D^{\ast}}-m_{DD^{\ast}}=142.00\,\mathrm{MeV}
$$

reproduce the standard $D^{\ast}{-}D$ spin gap. We do not claim a MELT
mapping for this gap in this note.

## 5. What the Public Data Say Before the Full Fit

The open Zenodo files were downloaded and checked locally. The selected
dataset contains $3{,}363{,}943$ unbinned dimuon mass values. It is dominated by
the $J/\psi$ and $\psi(2S)$ regions:

| Diagnostic | Value |
|---|---:|
| event count | $3{,}363{,}943$ |
| median mass | $3097.328\,\mathrm{MeV}/c^2$ |
| 1st percentile | $3074.131\,\mathrm{MeV}/c^2$ |
| 99th percentile | $3693.694\,\mathrm{MeV}/c^2$ |

A naive side-window scan is useful only as a diagnostic. It shows:

| Marker | Raw side-window result |
|---|---:|
| $J/\psi$ symmetric check | $\log_2(R/L)=-0.023$ |
| $DD^{\ast}$, 50 MeV windows | $\log_2(R/L)=-0.459$ |
| $DD^{\ast}$, 100 MeV windows | $\log_2(R/L)=-0.714$ |

The $DD$ and $\psi(3770)$ windows are contaminated by the huge $\psi(2S)$ tail
on the left side, so their raw count jumps should not be interpreted as
threshold physics.

A deliberately crude binned Poisson smoke test was also run over
$3760$ to $4250\,\mathrm{MeV}/c^2$. It compared a smooth continuum plus broad
Gaussian resonance anchors with and without a sigmoid step at $DD^{\ast}$. The
fitted step direction was negative, but the added step was not favored by
AIC/BIC:

$$
\Delta\mathrm{AIC}=+1.845,\qquad
\Delta\mathrm{BIC}=+4.429,
$$

with fitted step amplitude $-0.590$ in that crude model.

This is not a contradiction of the LHCb result. It is the useful lesson. The
$DD^{\ast}$ effect is not a raw histogram bump. It is an amplitude-level
Wilson/nonlocal effect. That is precisely why it is interesting as a MELT
ledger object.

## 6. Falsification and Next Work

The MELT reading is a structured hypothesis with clear failure modes.

It weakens if:

1. a reproduction of the LHCb likelihood absorbs the $DD^{\ast}$ step into
   smooth charm-loop modelling once the $X(3872)$ admixture is included
   explicitly;
2. the step moves away from the vector coefficient when alternative form
   factors are used;
3. the annular $(C_V,C_A)$ profile disappears in a more complete likelihood;
4. analogous $b\to s\mu^+\mu^-$ channels with similar charm-threshold reach
   show no comparable vector-specific gate.

It strengthens if:

1. the $DD^{\ast}$ response remains vector-specific under HPQCD/FNAL-MILC
   variation;
2. an explicit $X(3872)\to J/\psi\,\rho$ amplitude in the nonlocal model
   absorbs the step at a magnitude consistent with measured
   $\mathcal{B}(X(3872)\to J/\psi\,\rho)$;
3. analogous threshold-charmonium-vector-meson alignments
   (e.g. $B^0\to K^{\ast0}\mu^+\mu^-$ at the same $m_{\mu\mu}$ threshold)
   reproduce the gate;
4. the $C_A(q^2)$ drift remains as a gradual scale term while $C_V$ carries
   the discrete threshold gate.

The next technical steps are concrete:

1. **Reading-uncertainty reduction.** Extract the absolute $(C_V^\mathrm{fit},
   C_A^\mathrm{fit})$ from the published likelihood support files or from a
   local refit, replacing the $\pm 0.2$ visual readings used in §2.3 and §3.
   Only then should $\Delta C_V/0.8901$ be promoted from "scale check" to
   "quantitative claim."
2. **Minimal charm-window refit.** A binned-Poisson or unbinned amplitude
   reproduction over $3400$ to $4250\,\mathrm{MeV}/c^2$ using the published
   efficiency and resolution curves: smooth continuum, $\psi(2S)$,
   $\psi(3770)$, $\psi(4040)$, $\psi(4160)$, and either a $DD^{\ast}$ sigmoid
   gate or an explicit $X(3872)$ Breit–Wigner with its measured $J/\psi\,\rho$
   coupling.
3. **Cross-channel $X(3872)$ test.** Check whether $B^0\to K^{\ast0}\mu^+\mu^-$
   shows the same $C_V$ step at $m_{\mu\mu}=m_{X(3872)}$.

### References and Framework Anchors

- LHCb collaboration, *Measurement of the local and nonlocal amplitudes in
  $B^+\to K^+\mu^+\mu^-$ decays*, arXiv:2603.12477 (LHCb-PAPER-2025-055).
- LHCb public data release for the above paper, Zenodo
  DOI `10.5281/zenodo.19497184` (LHCb's data, used here only for diagnostics).
- Particle Data Group, $\chi_{c1}(3872)/X(3872)$ listing:
  $m=3871.64\pm0.06\,\mathrm{MeV}/c^2$, $J^{PC}=1^{++}$, with $J/\psi\,\rho^0$
  and $D^0\overline{D}{}^{\ast 0}$ decay channels.
- MELT bridge inventory: CP³+CP⁴+CP⁵ = 28+0+4 = 32 bit
  (hadron-bus / domain-wall / lepton-bus).
- MELT ballast-bit anchor: $K_S$ first-split Shannon entropy
  $H_1=0.8901\,\mathrm{bit}$.
- MELT Born/off-diagonal inventory: modulus readout versus retained
  off-diagonal phase.
