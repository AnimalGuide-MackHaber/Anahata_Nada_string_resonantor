# Part 4.3: Spatial Placement and Eddy Shields

When assembling an individual-pole driver (using six steel slugs and six Neodymium discs), the physical orientation of the permanent magnet relative to the coil completely dictates the driver's efficiency. 

If you place the Neodymium disc on **top** of the steel slug (facing the string) rather than on the **bottom**, you trigger dual catastrophic failures: The Eddy Shield Effect and Exponential Damping.

## 1. The Conduit vs. The Shield

As established, Neodymium is highly electrically conductive. Your coil generates its alternating magnetic field ($B_{ac}$) primarily at the top and bottom openings of the bobbin.

### The Correct Way: Bottom Placement (The Conduit)
*   **The Physics:** The Neodymium sits at the bottom. The steel slug sits inside the coil. 
*   **The Benefit:** The steel slug acts as a high-permeability magnetic conduit. It absorbs the massive static flux ($B_0$) from the Neodymium and carries it cleanly up to the string. The conductive mass of the Neodymium is kept relatively far away from the densest part of the expanding $B_{ac}$ field, minimizing eddy current heat.

### The Fatal Flaw: Top Placement (The Eddy Shield)
*   **The Physics:** The Neodymium sits on top of the slug, resting between the top of the coil and the guitar string.
*   **The Shielding Effect (Faraday & Lenz):** Before the $B_{ac}$ field can reach the string, it must physically pass through the highly conductive Neodymium disc. The alternating field instantly induces massive, swirling eddy currents inside the disc. These currents generate a perfect opposing magnetic field that cancels out your coil. 
*   **The Result:** The Neodymium disc acts as a solid electrical shield. It absorbs your Class D amplifier's energy, converting it entirely into raw heat and preventing the drive signal from ever reaching the string.

```mermaid
graph TD
    subgraph Top-Mounted Neodymium Failure
    direction TB
    A[String / Tine]
    B[Neodymium Disc <br> (Conductive Shield)]
    C[AC Coil Field B_ac]
    
    C -->|Field Attempts to Rise| B
    B -->|Absorbs AC / Generates Heat| B
    B -.-x|Field Choked / Blocked| A
    end
    
    style B fill:#991b1b,stroke:#fca5a5,color:#fff
    style C fill:#1e40af,stroke:#93c5fd,color:#fff
```

## 2. Exponential Proximity Damping

The static magnetic pull ($F_{pull}$) exerted on a steel string follows the inverse-square law based on distance ($d$):
$$F_{pull} \propto \frac{B_0^2}{d^2}$$

If you mount the Neodymium disc on top of a standard 15mm tall steel slug, you have physically moved the source of the massive static field 15mm closer to the strings.

*   **The Choke-Out:** To get the top of the driver close enough to push the string with the (now severely shielded) AC field, the Neodymium disc will end up sitting 1.0mm to 2.0mm away from the string.
*   **The Result:** Because distance is squared in the denominator, halving the distance roughly quadruples the pull. The static pull becomes so violently strong that the string will physically snap down, lock against the magnet, and refuse to vibrate.

**The Engineering Verdict:** You must keep Neodymium discs at the **bottom** of the steel slugs. This allows the steel to act as a focused conduit while keeping the conductive Neodymium mass out of the direct path of the AC coil field.