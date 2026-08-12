# Bottle-Spinner

A virtual Bottle Spinner designed to recreate the suspense and unpredictability of a physical bottle spin directly in the browser.

Bottle-Spinner uses browser cryptographic randomness to determine each spin independently, followed by a physics-inspired animation designed to make the outcome feel organic rather than mechanically predictable.

## Features

- Cryptographically secure randomization
- Independent 50/50 spin-direction selection
- Physics-inspired rotational animation
- Variable acceleration and deceleration
- Natural wobble and settling
- Five-spin rolling no-repeat system
- Responsive desktop and mobile layout
- Click or tap anywhere to spin
- No external libraries
- No server required
- Entire application contained in a single HTML file
- Bottle artwork embedded directly into the HTML

## Randomness

Bottle-Spinner uses the browser's `crypto.getRandomValues()` API as its primary source of randomness.

The visual animation does not determine the result.

The outcome is generated first, and the animation subsequently produces a visual trajectory toward that predetermined outcome. This prevents the animation itself from secretly deciding where the bottle lands.

The five-spin system intentionally prevents the landing angle from repeating within the previous five spins. This is a deliberate suspense feature rather than unrestricted physical randomness.

## Privacy

Bottle-Spinner does not require an account, backend, database, or external service to operate.

No personal information is required to use the spinner.

## Deployment

Bottle-Spinner is designed to run as a static website.

The entire application can be deployed using GitHub Pages with:

    index.html

No build process or package installation is required.

## Repository Structure

    spinner/
    ├── index.html
    ├── README.md
    ├── LICENSE
    └── .gitignore

## Browser Compatibility

Bottle-Spinner is designed for modern browsers supporting:

- JavaScript
- `crypto.getRandomValues()`
- `requestAnimationFrame()`
- Pointer Events
- CSS transforms

It is intended to work across desktop, tablet, and mobile devices.

## License

The source code is released under the MIT License.

Nuka Cola, Fallout, associated names, imagery, trademarks, and other intellectual property are the property of their respective owners. This project is not affiliated with or endorsed by Bethesda or any other rights holder.

## Project

**Bottle-Spinner**

A small experiment in making a browser-based randomizer feel physical, suspenseful, and difficult to predict.
