### D. W. Allan, N. Ashby, C. C. Hodge – The Science of Timekeeping (HP App Note 1289)

Evolution of precise timekeeping
- Quartz oscillators - first mass practical precision (radio, radar, TV, computers).
  - Define cycles via mechanical/electrical resonance.
  - Basis for everyday devices (phones, cars, appliances).
- Atomic clocks - higher accuracy, long-term stability.
  - EM transitions define frequency; became the main reference for navigation (GPS).
  - Accuracy today: $\pm 0.3$ ns/day

Natural clocks:
- Millisecond pulsars - astrophysical clocks.
  - periods $\approx 1.5578$ ms ($\approx 642$ rotations/s)
  - stability $\approx$ atomic clocks (error < 1s per well over a million years)
  - Observed via radio pulses (phase-stable EM signal)
  - Used with GPS for calibration
  - Potential tool for gravitational wave detection
- Earth’s rotation (original natural clock, now one of many layers).
  - Integrated in UTC corrections (leap seconds).

All timekeeping systems
- Observable periodic signal (mechanical, electromagnetic, rotational)
- Key measurable quantities: frequency and phase
- drift, noise, stability metrics define quality
- hierarchy of calibrations: natural phenomena -> atomic standards -> quartz devices -> network synchronization

Almost any clock - a two-part system:
- oscillating device - gives periodic events
- counter - adds them up, gives time

(pendulum: oscillation defines second, gears + clock face = counter part; atomic clock: oscillation = EM signal from transition between 2 energy levels)

A clock measures time by counting cycles of something that repeats regularly, after initial setting it keeps “its own” time by accumulating cycles, 

Clock quality (These measures are not all independent.)

**frequency accuracy** (=fractional or normalized frequency departure) - how well it realizes the second
- y(t) = (change in time error) / elapsed time
- Harrison chronometer goal: $y(t) < 3.5 \cdot 10^{-5}$
- today’s primary standards $\approx 10^{-14}$
- smaller y(t) - better clock
  
**frequency stability** - how much frequency changes from one time to next
- can be inaccurate but still stable (e.g. gains 1 s/day constantly - stable but inaccurate)
- examples:
  - hydrogen maser clock - better short-term stability
  - cesium-beam clock - more accurate
  - quartz-oscillator based clock - good short-term, drifts long-term

**time accuracy** - how well agrees with UTC
- ex: GPS satellites need clocks synchronized within few ns
- same for telecom networks - lost data if unsynced

**time stability** - how much the clock’s time changes compared to a perfectly uniform flow of time (usually correlated with frequency stability)
- example: clock gains 1 s/day everyday
  - its time accuracy is getting worse (drifts 1 s daily)
  - but its frequency stability is perfect — it always gains the same 1 s each day
  - => consequently perfect time predictability, if the time or frequency errors are known- one can correct them


Calibration hierarchy
  - Primary Frequency Standard - can define the second independently
  - not always running continuously
  - secondary clocks are calibrated to them
  - keep time when primary isn’t operating

Clock ensemble 
- 2 clocks - can tell difference, not which is wrong
- 3 (triangular comparison) allow estimating individual stabilities.
- 4 - redundancy (in case one fails)
- reliability + detect who’s “lying”
- Ensemble = weighted combination of several clocks (improves both reliability and stability).
- Even a bad clock can help if properly weighted (statistical averaging)
- Result = a “virtual” clock output more stable than any single clock.
  
Comparison methods
- Clocks compared via time/frequency transfer links; goal - minimal added noise
- Satellite-based (e.g. GPS) provides accuracies $< 1\mu s$ vs UTC
- Propagation delay (signal travel time) matters — nanoseconds for local, tens of ms for satellites.
- Accuracy limited by
  - Measurement noise
  - Internal clock deviations
  - Environmental perturbations.
- Transfer noise must be ≪ clock noise.

Triangular and larger networks
- Pairwise comparison: only gives relative differences.
- Triangular network (3 clocks): can solve for individual variances assuming uncorrelated noise.
  - for 3 clocks: $\sigma_1^2 = \frac{1}{2}(\sigma_{12}^2 + \sigma_{13}^2 - \sigma_{23}^2)$, similar for $\sigma_2$ and $\sigma_3$
- for larger networks - allows consistent estimation of all clocks’ stability even without external reference.
  
Synchronization
- The times of clocks are in synchronization if their
readings are the same after accounting for reference
frame delays and relativistic effects. Synchronization
needs to be specified to within some level of uncertainty.

GPS
- Provides both time transfer and time reference across locations
- types of time from GPS
  - GPS time
  - UTC estimated/produced by USNO
  - Individual free-running GPS satellite clocks
- Master Control Station (Falcon AFB) collects data from 5 global monitor stations
- Uses Kalman filter to estimate:
  - time error
  - frequency error
  - frequency drift
  - satellite orbital parameters
- updates sent to satellites - broadcasts synchronized GPS time across constellation.
- Result: GPS time consistency within a few nanoseconds, satellite positions within a few meters.
- Use multiple independent sources (satellites, timing centers) - redundancy improves reliability.
- Continuous error estimation and correction (Kalman filtering, predictions) - resilience to drift or failure.
- Broadcasting corrections allows remote nodes to compute accurate UTC - robust synchronization even if some signals are degraded.
- Ability to filter intentional/unintentional noise improves network robustness.

GPS vs UTC
- GPS time does not include leap seconds, while UTC does.
- Steering GPS time to match UTC(USNO MC) keeps differences > 40ns
- Enables receivers to calculate accurate UTC estimates, goal $\approx$ 28 ns

### Fritz Riehle, Frequency Standards: Basics and Applications, Wiley‐VCH Verlag GmbH & Co. KGaA, 2003.

Passive and active frequency standards
- passive
  - device/material sensitive to certain frequency(ies)
  - e.g. resonators, atoms in absorber cell
  - needs external oscillator, When interrogated by a suitable oscillator -> an absorption line at the resonance frequency $\nu_0$
  - symmetric absorption -> can derive anti-symmetric error signal $S$
  - used in servo loop to tune oscillator ($\nu \approx \nu_0$)
  - when loop closed, oscillator freq “locked” to reference -> stable
  - can be used as frequency standard if $\nu$ known + stable
- active
  - system itself produces radiation at given freq (no external drive)
  - e.g. excited atoms emitting coherent signal
  - examples: hydrogen maser, gas laser (He-Ne)

Frequency standart - clock
- can be used as a clock if the frequency is suitably divided in a clockwork device and displayed 
- example - a wrist watch where a quartz resonator defines the frequency of the oscillator at 32768 Hz = $2^{15}$ Hz that is used with a divider to generate the pulses for a stepping motor that drives the second
hand of the watch
- (oscillator + divider + display = clock)

If the frequency of a particular stable device has been measured by comparing it to the frequency of another source that can be traced back to the frequency of a primary standard used to realise the SI unit, our stable device then – and only then – represents a frequency standard.

Accuracy, stability analogy (fig 1.4 p.4)
- bullet holes - repeated frequency measurements
- a: tight cluster at centre - stable + accurate -> ideal standard
- b: wide scatter but centred -> poor short-term stability, good long-term accuracy
- c: tight cluster but offset -> stable but inaccurate (systematic offset, can still use if offset known + corrected)
- d: scattered + off-centre - unstable + inaccurate => unusable as standard
- relative accuracy/stability = deviation / $\nu_0$ - smaller number = better performance

**accuracy:** conformity of measured value to definition
**precision:** how well repeated measurements agree
  


### Petit & Tavella – “Atomic Timekeeping from 1955 to the Present” (2017)

“Defining a clock” = picking measurable periodic observable (rotation, oscillation, resonance).

Clock comparison
- to build global time scale need methods to compare distant clocks.
- must not degrade stability (transfer noise must be << clock noise).
- uncertainty for best modern links = few ns to 1 ns.
- frequency comparison: random/statistical uncertainty (Type A)
- time comparison: also systematic (Type B) from calibration (repeated calibrations crucial)
- comparison defines clock's stability
- It's possible to measure stability without knowing absolute accuracy

TAI, UTC, GPS
- TAI - International Atomic Time, pure atomic scale.
- UTC - Coordinated Universal Time, hybrid: atomic time + steps to follow Earth’s irregular rotation.
- UTC(k) - local approximation of UTC, traceable to UTC.
- Difference [TAI − GPS] = 19s + C (C $\approx$ 10)
- GPS clocks steered to UTC(USNO); maximum deviation <= 1$\mu s$
- even with perfect clocks, knowledge of absolute time depends on transmission, measurement, and reference uncertainties
- UTC approximates solar time, TAI approximates ideal atomic time; we cannot directly observe “absolute” time
- Measurement precision is limited by physical signals, environmental effects, and fundamental stochastic clock noise



### W. J. Riley, Handbook of Frequency Stability Analysis, NIST SP 1065.

Drift
- Systematic change in frequency over time (from all causes).
- Differs from aging: aging = internal effects only; drift = internal + external.
- Example: quartz oscillator: aging = crystal changes; drift = aging + environmental influence.
- Drift usually measured under stable conditions (to isolate aging).
- To analyze: fit trend (linear, log, etc.) using least squares -> remove systematic part before noise analysis.
- Good model = leaves white (uncorrelated) residuals.

Noise
- wave output signal from frequency source: $V(t) = [V_0 + \varepsilon (t)]\sin[2\pi \nu_0 t + \phi(t)]$ ($V_0$ - nominal peak output voltage, $\varepsilon (t)$ -  amplitude deviation, $\nu_0$ - nominal frequency, $\phi (t)$ - phase deviation)
- instantaneous frequency: derivative of total phase.
- Fractional frequency (relative frequency deviation): $y(t)=\frac{1}{2\pi\nu_0}\frac{d\phi}{dt}$
- Have power-low type with spectral density $S_y(f) \propto f^\alpha$
- types
  - $\alpha=2$ - White PM (W PM) 
  - $\alpha=1$ - Flicker PM (F PM)
  - $\alpha=0$ - White FM (W FM)
  - $\alpha=-1$ - Flicker FM (F FM)
  - $\alpha=-2$ - Random Walk FM (RW FM)
  - $\alpha=-3$ - Flicker Walk FM (FW FM)
  - $\alpha=-4$ - Random Run FM (RR FM) 