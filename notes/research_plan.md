### 1. Defining a clock

**What observable property (phase, frequency, rotation, signal) makes your chosen system measurable as a clock?**

A clock measures time by counting cycles of a repeating process (oscillation, rotation, resonance, etc.).

The measurable property is frequency (or equivalently phase), which can be tracked over time.
  
**How does its *stability* differ from its *accuracy*?**

Accuracy – how close the mean frequency is to the true or defined value (SI second).

Stability – how little the frequency changes with time.

A clock can be stable but inaccurate

Stability is needed for predictability; accuracy needs calibration.
  
**Can a clock exist without being compared to another?**

Yes, but only in a relative sense.

A single clock can keep its own time, but accuracy can’t be known without comparison. (it's only possible to measure stability internally, but not accuracy)

### 2. Benchmarking and Comparison

**How can we compare clocks without an external reference?**

By comparing differences between clocks.
Two clocks - only relative drift (can’t tell which one is off).
With more clocks, individual stabilities can be solved statistically.

**What does a *triangular* comparison network achieve that pairwise comparisons do not?**

With 3 clocks and all pairwise differences, it's possible to separate the contribution of each clock:
($\sigma_1^2 = \frac{1}{2}(\sigma_{12}^2 + \sigma_{13}^2 - \sigma_{23}^2)$)

=> Each clock’s individual noise/stability can be estimated without a reference.

Also helps detect which clock is unstable (if one’s variance dominates).

**How could this concept generalize to more complex networks?**

Use all pairwise comparisons to fit consistent variances.

Outlier detection: unstable clock can be identified and down-weighted.

Weighted average (“ensemble time”) gives a virtual clock more stable than any single one.

### 3. Extending the Scope

**How might atomic clocks, quartz oscillators, Earth’s rotation, or pulsars all fit into a common timekeeping model?**

All of them are oscillators with measurable periodic behaviour.

Atomic clock: EM transition between energy levels - defines the SI second.

Quartz oscillator: mechanical/electrical resonance - cycles counted electronically.

Earth’s rotation: rotational period as natural “day” standard - basis of mean solar time.

Pulsar: neutron star rotation - stable periodic EM pulses.

Common structure: periodic process + counter

Timekeeping hierarchy: natural phenomena (Earth, pulsar) -> atomic standards -> quartz devices -> network synchronization

**Which observables (frequency drift, phase noise, orbital period, etc.) unify these systems conceptually?**

Frequency – how many cycles per unit time.

Phase – position within each cycle.

Drift – systematic change in frequency over time.

Noise/stability metrics – quantify short-term and long-term variations.

Period stability – from seconds (quartz) to years (pulsars).

All clocks can be modeled as: $V(t) = [V_0 + \varepsilon (t)]\sin[2\pi \nu_0 t + \phi(t)]$ ($V_0$ - nominal peak output voltage, $\varepsilon (t)$ -  amplitude deviation, $\nu_0$ - nominal frequency, $\phi (t)$ - phase deviation)

### 4. Numerical Realization
   - **Which aspects of your chosen model can be simulated with realistic noise parameters?**
   - **What assumptions will you make about noise types (white, flicker, random-walk)?**
   - **How can you visualize the performance and correlations within your network?**

### 5. Interpretation and Broader Context
   - **What does “synchronization” mean when combining systems from quantum to cosmological scales?**
   - **How might such models inform the design of a *resilient global time network*?**
   - **What are the epistemic limits of measuring time itself?**


I will simulate three clocks with different noise models (white, flicker, and random walk) and study how these affect their long-term stability using Allan deviation.