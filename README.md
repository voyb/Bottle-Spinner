Bottle-Spinner

A virtual bottle spinner designed to recreate the suspense and unpredictability of a physical bottle spin directly in the browser.

Features
Cryptographically secure randomness
Physics-based forward simulation
Two-phase friction model
Natural acceleration and deceleration
50/50 spin direction
No predetermined landing angle
Five-spin no-repeat system
Responsive desktop and mobile design
Click or tap anywhere to spin
No external libraries
No server required
Single HTML file
Physics

The bottle's final angle is determined through forward physics simulation using randomly generated physical parameters rather than a predetermined target angle.

The simulation uses:

Initial angular velocity (ω₀)
Viscous friction (μV)
Coulomb friction (μC)

The bottle begins with rotational energy and naturally loses that energy through a two-phase friction model:

Viscous friction at high rotational speeds
Coulomb friction as the bottle slows toward rest

The bottle is never told where it should land. It simply runs out of rotational energy and stops wherever the simulation takes it.

Randomness

Each spin uses multiple independent sources of entropy:

2 × 64-byte CSPRNG blocks
Environmental timing noise
performance.now()
requestAnimationFrame() timing
Screen dimensions and device metrics
Hardware concurrency
Double SHA-256 hash mixing
Independent hash regions for each physics parameter

The physics parameters are derived independently from the resulting hash material.

The spin direction is determined by a single cryptographically secure random bit, giving an even 50/50 clockwise or counter-clockwise selection under the CSPRNG model.

License

MIT License.

Project

Bottle-Spinner

A lightweight browser-based experiment combining cryptographic randomness and forward physics simulation to create a bottle spinner that does not select a predetermined landing position.
