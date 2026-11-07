# Automatic Night-Activated Twilight Switch (BJT + Photoresistor)

An analog automatic switch designed and simulated in **Autodesk Tinkercad Circuits** (https://www.tinkercad.com/things/f7u9WAquaxd/editel?returnTo=%2Fdashboard%2Fdesigns%2Fall&sharecode=yFGrGuAplPh9DQV7klbVtF8GFtogdW0SA06VKsNwsHo). The circuit monitors ambient illumination using a photoresistor (LDR) and automatically powers an LED indicator at night while remaining off during daylight hours.

---

## 1. Project Specifications & Requirements

* **Environment:** Autodesk Tinkercad (Circuits Module)
* **Objective:** Design an autonomous switch that energizes an illumination load in low-light/night conditions and automatically turns off in daytime/ambient light conditions.
* **Allowable Components:** 
  * 9V DC Battery / Power Supply
  * Bipolar Junction Transistor (NPN BJT)
  * Photoresistor (CdS Light Dependent Resistor / LDR)
  * Carbon film resistors (divider network and current-limiting stages)
  * Standard LED (Illumination load)

---

## 2. Complete Circuit Schematic & Architecture

```text
       +9V DC Rail (VCC)
          │
    ┌─────┴────────────────────────┐
    │                              │
   [R1] 10 kΩ                      │
    │                              [R2] 680 Ω (Current Limiting Resistor)
    ├─────────────────┐            │
    │                 │          ┌─┴─┐
   [ ]                │          │ A │ Standard Red LED
  Photo-              │          │ K │ (Anode -> Cathode)
  resistor (LDR)      │          └─┬─┘
    │               [Base]         │
    │              ┌──┴──┐         │
    │              │ BJT │◄────────┘ (Collector)
    │              └──┬──┘
    │               [Emitter]
    │                 │
────┴─────────────────┴──────────── Ground (0V / Negative Rail)
