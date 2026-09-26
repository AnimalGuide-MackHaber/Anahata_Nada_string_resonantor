# Part 1.1: The Closed-Loop Feedback System (Ahata vs. Anahata)

## 1. The Acoustic Philosophy
Traditional acoustic instruments operate on the principle of **Ahata** (struck sound). Energy is injected once (via a pick, hammer, or finger), transferred to the surrounding air, and immediately begins to decay. The instrument acts as a decaying mechanical oscillator.

The Sympathetic Electromagnetic Array is designed to achieve **Anahata** (the un-struck, infinite vibration). It intercepts the decaying acoustic energy, amplifies it, and actively forces it back into the steel, creating a self-sustaining system that relies on continuous electrical power rather than a single kinetic strike.

## 2. The Electromechanical Loop Equation
To achieve infinite sustain, the system relies on the **Barkhausen Criterion** for oscillation, adapted for electromechanics. The total loop gain ($A_{loop}$) must be greater than or equal to $1$, and the phase shift around the loop must be a multiple of $360^\circ$ ($2\pi$).

$$A_{loop} = G_{piezo} \cdot G_{amp} \cdot G_{coil} \cdot G_{mech} \ge 1$$

Where:
*   $G_{piezo}$ = Efficiency of the receiver converting kinetic string motion to AC voltage.
*   $G_{amp}$ = Voltage gain of the Class-D amplifier.
*   $G_{coil}$ = Efficiency of the driver converting AC voltage into magnetic flux ($B_{ac}$).
*   $G_{mech}$ = Mechanical coupling of the magnetic flux physically moving the string.

If $A_{loop} < 1$, the string decays. If $A_{loop} > 1$, the string violently accelerates until it reaches physical maximum excursion (clipping against the frets or driver).

## 3. The Energy Circuit Architecture
The system is fundamentally an energy conversion loop. Understanding where the bottlenecks occur is critical for engineering the chassis.

```mermaid
graph TD
    A[Kinetic Energy <br> Vibrating Steel] -->|Piezoelectric Effect| B(AC Micro-Voltage)
    B -->|Pre-Amp Buffer| C{Class-D Audio Amplifier}
    C -->|High Current AC| D[Electromagnetic Driver]
    D -->|Ampere-Turns to Flux| E(Expanding/Collapsing Magnetic Field)
    E -->|Lorentz Force Push/Pull| A
    
    style A fill:#1e40af,stroke:#93c5fd,stroke-width:2px,color:#fff
    style C fill:#065f46,stroke:#6ee7b7,stroke-width:2px,color:#fff
    style D fill:#991b1b,stroke:#fca5a5,stroke-width:2px,color:#fff
```

### Time Domain: Standard Decay vs. Infinite Sustain
```mermaid
xychart-beta
    title "Time Domain: Amplitude Over Time (Ahata vs Anahata)"
    x-axis "Time (Seconds)" [0, 1, 2, 3, 4, 5, 6]
    y-axis "String Excursion (Amplitude)" 0 --> 100
    line [95, 45, 20, 10, 4, 1, 0] 
    bar [10, 85, 95, 95, 95, 95, 95]
```
*(Line: Standard Acoustic Decay | Bars: Active Electromagnetic Sustain achieving Anahata).*