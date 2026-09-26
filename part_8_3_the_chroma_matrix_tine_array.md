# Part 8.3: The "Chroma Matrix" Tine Array Fabrication

If you implement the **Cantilever Music Wire Array** (mounting rigid tines over a P90 driver), you are no longer constrained by tuning pegs or scale length. The pitch is dictated entirely by where you cut the wire. 

Because we want this array to sympathetically respond to whatever audio signal you pump into the driver, the tines must be cut to perfectly cover a wide range of musical frequencies.

## 1. The .047" Master Length Equation
As calculated in Part 2.2 (Cantilever Physics), the fundamental frequency for a solid steel cylinder is dictated by its stiffness and mass. For your specific **0.047 inch (1.19 mm)** high-carbon steel wire, the workshop formula to find the required length ($L$) for any frequency ($f$) is:

$$L \text{ (in millimeters)} \approx \frac{1045}{\sqrt{f}}$$

## 2. The 16-Tine Matrix Cut List
A standard P90 bobbin is roughly 3 inches wide. You can comfortably fit 16 tightly spaced tines across this magnetic aperture.

This array spans three octaves (G2 to G5) and is heavily weighted toward roots, fifths, and octaves, ensuring maximum sympathetic excitation.

*Fabrication Warning: Always cut the wire **5mm longer** than listed. You must physically tune the tines by filing or grinding the tips down once they are clamped, as the magnetic pull of the driver will alter their final resting pitch.*

| Tine # | Target Note | Frequency (Hz) | Required Free Length ($L$) | Musical Tonality |
| :--- | :--- | :--- | :--- | :--- |
| **1** | G2 | 98.00 Hz | **105.5 mm** (4.15") | Low Fundamental |
| **2** | A2 | 110.00 Hz | **99.6 mm** (3.92") | Major 2nd Tonality |
| **3** | C3 | 130.81 Hz | **91.4 mm** (3.60") | Root for C/Am Chords |
| **4** | D3 | 146.83 Hz | **86.2 mm** (3.39") | Perfect 5th (above G) |
| **5** | E3 | 164.81 Hz | **81.4 mm** (3.20") | Major 3rd Tonality |
| **6** | G3 | 196.00 Hz | **74.6 mm** (2.94") | Midrange Root |
| **7** | A3 | 220.00 Hz | **70.4 mm** (2.77") | Standard Drone (A440/2) |
| **8** | C4 | 261.63 Hz | **64.6 mm** (2.54") | Middle C Anchor |
| **9** | D4 | 293.66 Hz | **61.0 mm** (2.40") | High Perfect 5th |
| **10** | E4 | 329.63 Hz | **57.6 mm** (2.27") | High Major 3rd |
| **11** | G4 | 392.00 Hz | **52.8 mm** (2.08") | High Octave |
| **12** | A4 | 440.00 Hz | **49.8 mm** (1.96") | A440 Standard |
| **13** | C5 | 523.25 Hz | **45.7 mm** (1.80") | High Chime |
| **14** | D5 | 587.33 Hz | **43.1 mm** (1.70") | Piercing Overtone |
| **15** | E5 | 659.25 Hz | **40.7 mm** (1.60") | Piercing Overtone |
| **16** | G5 | 783.99 Hz | **37.3 mm** (1.47") | "Air Band" Resonance |

## 3. Clamping and Magnetic Clearance
*   **The Clamp Base:** The tines must be sandwiched between two heavy blocks of solid metal (e.g., 1/4" steel flat bar) securely bolted together. If you use wood, the wood fibers will absorb the vibration, and the tines will sound dull ("thud" instead of "ping").
*   **Magnetic Air Gap ($z$):** Because you are using Ceramic magnets for your 4-ohm P90 driver, the static pull is relatively gentle. You can mount the P90 so the pole pieces sit exactly **1.0mm to 1.5mm** directly underneath the free-floating tips of the 16 tines to maximize the AC field transfer.