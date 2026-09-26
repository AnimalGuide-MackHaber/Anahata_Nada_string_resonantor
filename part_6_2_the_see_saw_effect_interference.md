# Part 6.2: The "See-Saw" Effect and Destructive Interference

While two drivers working in-phase ($+1$) perfectly amplify the fundamental wave, that exact same wiring configuration will catastrophically destroy specific high-frequency overtones.

This occurs because higher harmonics divide the string into multiple physical segments that vibrate in opposite directions simultaneously. 

## 1. The 3rd Harmonic Geometry (The Perfect 5th)
When a string vibrates at the 3rd harmonic ($n=3$), it physically divides into three equal "humps." 

Imagine freezing time at the exact millisecond this wave hits its peak amplitude.
*   The first hump (nearest the bridge) is swinging **UP**.
*   The second hump (the middle) is swinging **DOWN**.
*   The third hump (nearest the nut) is swinging **UP**.

## 2. The Cancellation Mathematics
Let's run the $F_{net}$ equation for the 3rd harmonic ($n=3$), keeping both drivers **In-Phase** ($+1$).
*   **Driver 1 (Neo @ $L/2$):** $C_{3,1} = \sin(3 \cdot \pi \cdot 0.5) = \sin(1.5\pi) = \mathbf{-1.0}$
*   **Driver 2 (Ceramic @ $L/6$):** $C_{3,2} = \sin(3 \cdot \pi \cdot 0.166) = \sin(0.5\pi) = \mathbf{1.0}$

**Calculate Vector Sum:**
$$F_{net} = (-1.0 \cdot 3.5 \cdot 1) + (1.0 \cdot 1.0 \cdot 1)$$
$$F_{net} = -3.5 + 1.0 = \mathbf{-2.5}$$

### The Mechanical Failure (Fighting the Wave)
Look closely at the math: The Neodymium driver is applying $-3.5$ units of force, while the Ceramic driver is applying $+1.0$ unit of force. 
*   **The Physics:** The two electromagnets are physically fighting each other. The Ceramic driver is trying to heave the string UP exactly while the Neodymium driver is trying to heave it DOWN. 
*   **The Result:** Because the Neodymium driver is so much stronger, it wins the fight, but a massive amount of kinetic energy is lost. This is called **Destructive Interference**. The 3rd harmonic is severely choked and will struggle to ring out.

### Spatial Domain: The See-Saw Fight
```mermaid
graph TD
    subgraph Destructive Interference (Drivers In-Phase)
    direction LR
    A[AC Signal +1] --> B[Driver 1: Center]
    A --> C[Driver 2: Bridge]
    
    B -->|Pushes String UP| D(String Center: Wants to go DOWN)
    C -->|Pushes String UP| E(String Bridge: Wants to go UP)
    
    D -->|Mechanical Conflict| F{Drivers Fight <br> Energy Wasted}
    E -->|Mechanical Match| F
    end
    
    style D fill:#991b1b,stroke:#fca5a5,color:#fff
    style E fill:#065f46,stroke:#6ee7b7,color:#fff
    style F fill:#991b1b,stroke:#fca5a5,color:#fff
```