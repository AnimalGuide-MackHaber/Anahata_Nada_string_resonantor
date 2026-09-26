# Appendices: Quick Reference

## Appendix A: Master Formula Cheat Sheet

### 1. Mechanical String Tension (Mersenne's Law)
To calculate the mechanical tension ($T$) in Newtons required to reach a specific pitch:
$$T = 4 \mu L^2 f^2$$
*(Shows why doubling scale length $L$ requires 4x the physical tension, providing the stability needed to resist Neodymium magnets).*

### 2. Spatial Coupling Coefficient ($C_n$)
To calculate the mechanical leverage (0.0 to 1.0) your driver has over any specific harmonic ($n$) based on its physical coordinate ($x$) on the scale length ($L$):
$$C_n = \left| \sin\left(\frac{n \cdot \pi \cdot x}{L}\right) \right|$$

### 3. Ohm's Law for Output Power
To calculate the maximum Class-D amplifier power output ($P$) in Watts based on your coil winding resistance ($R$) and the 5V power rail ($V$):
$$P = \frac{V^2}{R}$$
*(4 Ohms = ~3.0 Watts | 8 Ohms = ~1.5 Watts)*

### 4. Eddy Current Power Loss
To understand why laminated steel is required instead of solid steel for blades:
$$P_e \propto \frac{B^2 \cdot f^2 \cdot d^2 \cdot V}{\rho}$$
*(Because thickness $d$ is squared, reducing a 5mm blade to a 0.35mm lamination sheet drops parasitic heat loss by over 99%).*

---

## Appendix B: Multi-Driver Simulator Access
The mathematics of vector summation, interference, and spatial coupling can be complex to visualize on paper. 

A standalone HTML/JS simulator has been developed to visually map driver placement, phase inversion, and harmonic excitation across the scale length. 

**Filename:** `index.html` (Found in the root directory of this repository).
**Usage:** Open the file in any modern web browser to interactively slide drivers across the virtual chassis and view real-time $F_{net}$ calculations.