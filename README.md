# canary-health-monitor
Canary: astronaut self-baseline health monitor

On a Mars transit, the astronaut is the first responder. Canary compares every reading to the astronaut's own baseline, flags early drift, and explains what changed and what to do, even offline.

Live demo: https: https://canary-health-monitor.vercel.app/
Video: ADD AFTER FINISHING | Team: Krisha Gupta

Screenshot
<img width="1460" height="1010" alt="image" src="https://github.com/user-attachments/assets/8017c851-066c-48fa-ab4a-23263e557669" />

Problem

On long missions, Earth can be 20+ minutes away. Radiation, isolation, altered gravity, and closed environments affect health, so crews must self-assess. A population "normal range" misses changes that are small for one person but important for them.

Features
Personal baseline: median and MAD of days 1-7
Drift detection: two-sided CUSUM (k=0.5, h=4) per indicator
Fusion by body region: a region flags only when enough indicators drift together
Safety limits: illustrative absolute limits override the baseline
Clickable body, trend charts, and measurement guidance
Escalation by environment: station, lunar base, or Mars transit
Radiation tracker: running dose total against an illustrative budget, with a solar-event spike warning and manual dosimeter logging
Flight surgeon summary: one-click text summary of status, drift, safety limits, and radiation
Reaction check: five-tap test compared to baseline
Runs offline in the browser, no server
Run it

Open index.html or use the live demo. Drag the day slider or press Play mission.

Limitations
Data is simulated, with a planted drift
Thresholds are illustrative, not clinical
Decision support, not diagnosis
Radiation budget is illustrative, and false-alarm rate is not yet measured on large drift-free runs
Next steps

Validate on public sleep and reaction-time datasets, add Stroop and n-back tasks, and check thresholds against NASA references.

Sources
NASA Human Research Program: https://www.nasa.gov/hrp/
ADD MORE

MIT License
