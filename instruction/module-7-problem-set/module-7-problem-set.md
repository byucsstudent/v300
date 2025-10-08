# Module 7 Problem Set

This problem set is designed to reinforce your understanding of three-phase power systems, a crucial topic in electrical engineering. Working through these problems will solidify your knowledge of concepts like balanced and unbalanced loads, power calculations in three-phase circuits, and different connection configurations (wye and delta). Remember to review the lectures and readings from Module 7 as you tackle these problems. Good luck!

## Problem 1: Balanced Wye-Connected Load

A balanced, three-phase, wye-connected load is supplied by a 480V (line-to-line), 60 Hz source. Each phase of the load consists of a resistor of 20 ohms and an inductor with a reactance of 15 ohms, connected in series.

*   Calculate the phase voltage.
*   Calculate the phase current.
*   Calculate the line current.
*   Calculate the total three-phase apparent power (S), real power (P), and reactive power (Q) absorbed by the load.
*   What is the power factor of the load?

**Solution Approach:**

1.  **Phase Voltage:** In a wye connection, the phase voltage is the line-to-line voltage divided by the square root of 3.
2.  **Impedance:** Calculate the impedance of each phase using the resistance and reactance: Z = R + jX.  Then find the magnitude of the impedance: |Z| = sqrt(R² + X²).
3.  **Phase Current:** Calculate the phase current using Ohm's Law: I_phase = V_phase / |Z|.
4.  **Line Current:** In a wye connection, the line current is equal to the phase current.
5.  **Power Calculations:**
    *   Apparent power (S) = 3 * V_phase * I_phase
    *   Real power (P) = 3 * V_phase * I_phase * cos(θ), where θ is the angle of the impedance (arctan(X/R)).
    *   Reactive power (Q) = 3 * V_phase * I_phase * sin(θ)
6.  **Power Factor:**  Power factor (PF) = cos(θ) = P / S

**Common Challenges and Solutions:**

*   **Confusing Line and Phase Values:** Always remember the relationship between line and phase voltages and currents for both wye and delta connections. Refer back to the module notes for these relationships.
*   **Complex Numbers:** Using complex numbers correctly is crucial. Ensure you understand how to add, subtract, multiply, and divide complex numbers. A scientific calculator with complex number capabilities is highly recommended.
*   **Units:** Always include the correct units in your answers (e.g., Volts, Amps, Watts, VARs, VA).

## Problem 2: Delta-Connected Load

A balanced, three-phase, delta-connected load is connected to a 208V (line-to-line), 60 Hz source. Each phase of the load consists of a 10-ohm resistor in series with a 8-ohm inductor.

*   Calculate the phase voltage.
*   Calculate the phase current.
*   Calculate the line current.
*   Calculate the total three-phase apparent power (S), real power (P), and reactive power (Q) absorbed by the load.
*   What is the power factor of the load?

**Solution Approach:**

1.  **Phase Voltage:** In a delta connection, the phase voltage is equal to the line-to-line voltage.
2.  **Impedance:** Calculate the impedance of each phase using the resistance and reactance: Z = R + jX.  Then find the magnitude of the impedance: |Z| = sqrt(R² + X²).
3.  **Phase Current:** Calculate the phase current using Ohm's Law: I_phase = V_phase / |Z|.
4.  **Line Current:** In a delta connection, the line current is equal to the phase current multiplied by the square root of 3.
5.  **Power Calculations:**
    *   Apparent power (S) = 3 * V_phase * I_phase
    *   Real power (P) = 3 * V_phase * I_phase * cos(θ), where θ is the angle of the impedance (arctan(X/R)).
    *   Reactive power (Q) = 3 * V_phase * I_phase * sin(θ)
6.  **Power Factor:**  Power factor (PF) = cos(θ) = P / S

**Common Challenges and Solutions:**

*   **Remember the Delta Relationships:** Ensure that you apply the correct relationships between line and phase currents in a delta connection.
*   **Calculator Errors:** When dealing with square roots and trigonometric functions, double-check your calculator settings (degrees vs. radians).
*   **Understanding Power Factor:** A lagging power factor indicates an inductive load.

## Problem 3: Two-Wattmeter Method

A three-phase motor operating at 480V (line-to-line) draws 30A of line current and has a power factor of 0.8 lagging.  Two wattmeters are used to measure the total power consumed by the motor. Calculate the readings of each wattmeter.

**Solution Approach:**

1.  **Calculate Total Real Power:**  P = sqrt(3) * V_L * I_L * PF
2.  **Wattmeter Readings:** The readings of the two wattmeters (W1 and W2) can be calculated using the following formulas:
    *   W1 = V_L * I_L * cos(30° - θ)
    *   W2 = V_L * I_L * cos(30° + θ)
    where θ = arccos(PF)

**Common Challenges and Solutions:**

*   **Understanding the Two-Wattmeter Method:** This method is based on the principle that any three-phase power can be measured using only two wattmeters, regardless of the load balance.
*   **Correctly Calculating the Angle:** Make sure to use the correct angle θ, which is the angle whose cosine is the power factor.
*   **Interpreting Wattmeter Readings:** If one of the wattmeter readings is negative, it indicates a power factor less than 0.5.

## Problem 4: Unbalanced Wye-Connected Load

An unbalanced wye-connected load is connected to a balanced 208V (line-to-line) three-phase source. The impedances of the load are:

*   Za = 10 + j5 ohms
*   Zb = 15 - j10 ohms
*   Zc = 20 + j0 ohms

Assume a neutral wire exists. Calculate the line currents Ia, Ib, and Ic.

**Solution Approach:**

1.  **Phase Voltages:** Since the source is balanced and wye-connected, and a neutral wire exists, the phase voltages are equal to the line-to-line voltage divided by the square root of 3.  Also, the phase voltages are 120 degrees apart.  You'll need to express these in complex form.
2.  **Line Currents:** Calculate each line current by dividing the corresponding phase voltage by the corresponding impedance:
    *   Ia = Va / Za
    *   Ib = Vb / Zb
    *   Ic = Vc / Zc

**Common Challenges and Solutions:**

*   **Dealing with Unbalanced Loads:**  Unbalanced loads require individual calculation of each phase current. The presence of a neutral wire simplifies the analysis by maintaining a fixed neutral point voltage.
*   **Complex Arithmetic:**  This problem heavily relies on complex number arithmetic. Practice your complex number operations.
*   **Understanding Phase Sequence:** The phase sequence (ABC or ACB) affects the phase angles of the source voltages. Ensure you are using the correct sequence.

## Problem 5: Power Factor Correction

A three-phase induction motor draws 10 kW of power at a power factor of 0.75 lagging from a 480V (line-to-line), 60 Hz source. Calculate the capacitance per phase required to improve the power factor to 0.95 lagging. Assume a wye connected capacitor bank.

**Solution Approach:**

1.  **Calculate Initial Apparent Power:** S1 = P / PF1
2.  **Calculate Initial Reactive Power:** Q1 = sqrt(S1² - P²)
3.  **Calculate Target Apparent Power:** PF2 = 0.95, so S2 = P / PF2
4.  **Calculate Target Reactive Power:** Q2 = sqrt(S2² - P²)
5.  **Calculate Reactive Power to be Supplied by Capacitors:** Qc = Q1 - Q2
6.  **Calculate Capacitance per Phase:** Qc_phase = Qc / 3. Then, C = Qc_phase / (ω * V_phase²), where ω = 2πf and V_phase = V_L / sqrt(3).

**Common Challenges and Solutions:**

*   **Power Factor Correction Concepts:** Understand why power factor correction is important (reduces current, improves voltage regulation).
*   **Choosing the Right Components:** The choice of capacitors depends on voltage, frequency, and reactive power requirements.
*   **Units Conversion:** Be careful with units. Ensure that power is in Watts and VARs, voltage is in Volts, frequency is in Hertz, and capacitance is in Farads.

## Summary

This problem set provided practice in analyzing balanced and unbalanced three-phase systems, calculating power, and understanding the two-wattmeter method. Successfully completing these problems demonstrates a strong foundation in three-phase power system principles. Remember to review the solutions carefully and identify areas where you can improve your understanding. Continue practicing similar problems to further solidify your knowledge.
