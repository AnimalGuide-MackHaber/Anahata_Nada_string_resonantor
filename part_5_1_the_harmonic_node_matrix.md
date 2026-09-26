# Part 5.1: The Harmonic Node and Antinode Matrix

Because your strings (or fixed-fixed wire beams) are anchored rigidly at both ends (the nut and the bridge), they cannot vibrate freely like a wobbly rubber band. They are restricted to vibrating in mathematically locked standing waves, known as **Harmonics** ($n$).

When engineering a sustainer, the physical placement of your electromagnet dictates which of these harmonics will ring infinitely, and which ones will be instantly choked out.

## 1. Nodes vs. Antinodes

Every standing wave is composed of two distinct physical features:
*   **Nodes (The Dead Spots):** Points along the string where there is absolutely zero physical movement. The wave crosses the center line here. 
*   **Antinodes (The Sweet Spots):** Points along the string where the physical excursion (swing) is at its absolute maximum. 

If you place an electromagnetic driver directly under a **Node**, it is pushing against a brick wall. The magnetic field will try to heave the string upward, but because that specific coordinate is mathematically locked by the wave shape, the string will refuse to move. The driver efficiency drops to 0%.

## 2. The Harmonic Division Table

To successfully drive a specific overtone, the driver must be placed as close to an **Antinode** as possible. The following matrix maps out the exact physical fractions of your scale length ($L$) where these points occur.

| Harmonic ($n$) | Interval Name | Nodes (0% Efficiency) | Antinodes (100% Efficiency) |
| :--- | :--- | :--- | :--- |
| **1** | Fundamental (Root) | $0, L$ | **$L/2$** (Dead Center) |
| **2** | Octave | $0, L/2, L$ | **$L/4, 3L/4$** |
| **3** | Perfect 5th | $0, L/3, 2L/3, L$ | **$L/6, L/2, 5L/6$** |
| **4** | Double Octave | $0, L/4, L/2, 3L/4, L$ | **$L/8, 3L/8, 5L/8, 7L/8$** |
| **5** | Major 3rd | $0, L/5, 2L/5, 3L/5, 4L/5, L$ | **$L/10, 3L/10, L/2, 7L/10, 9L/10$** |
| **6** | Octave + 5th | $0, L/6, L/3, L/2, 2L/3, 5L/6, L$ | **$L/12, L/4, 5L/12, 7L/12, 3L/4, 11L/12$** |

## 3. The "Blind Spot" Phenomenon

Look closely at the **Node** column for the 2nd, 4th, and 6th harmonics (the even-order harmonics). Notice that they all share a node at exactly **$L/2$** (the dead center of the string).

*   **The Physics:** Even-order harmonics perfectly divide the string in half. 
*   **The Engineering Reality:** If you mount your driver exactly halfway between the bridge and the nut, the driver becomes completely "blind" to octaves. It cannot push them, and if an octave naturally tries to ring out, the center-mounted driver will actually dampen it.

```mermaid
graph TD
    subgraph The Mechanical Sieve (L/2 Placement)
    direction TB
    A[Driver Pumping AC Energy at L/2] --> B{Does a Node exist at L/2?}
    B -->|Yes| C[Even Harmonics: 2nd, 4th, 6th]
    B -->|No| D[Odd Harmonics: 1st, 3rd, 5th]
    C --> E(0% Energy Transfer - Choked)
    D --> F(100% Energy Transfer - Infinite Sustain)
    end
    
    style E fill:#991b1b,stroke:#fca5a5,color:#fff
    style F fill:#065f46,stroke:#6ee7b7,color:#fff
```