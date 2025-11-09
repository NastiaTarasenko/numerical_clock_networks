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
   - **How can we compare clocks without an external reference?**
   - **What does a *triangular* comparison network achieve that pairwise comparisons do not?**
   - **How could this concept generalize to more complex networks?**

### 3. Extending the Scope
   - **How might atomic clocks, quartz oscillators, Earth’s rotation, or pulsars all fit into a common timekeeping model?**
   - **Which observables (frequency drift, phase noise, orbital period, etc.) unify these systems conceptually?**

### 4. Numerical Realization
   - **Which aspects of your chosen model can be simulated with realistic noise parameters?**
   - **What assumptions will you make about noise types (white, flicker, random-walk)?**
   - **How can you visualize the performance and correlations within your network?**

### 5. Interpretation and Broader Context
   - **What does “synchronization” mean when combining systems from quantum to cosmological scales?**
   - **How might such models inform the design of a *resilient global time network*?**
   - **What are the epistemic limits of measuring time itself?**


I will simulate three clocks with different noise models (white, flicker, and random walk) and study how these affect their long-term stability using Allan deviation.