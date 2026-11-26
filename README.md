# Sequential 3-LED Controller (Arduino)

A beginner Arduino project that lights up three LEDs—Green, Red, and Blue—one after another in a repeating loop[cite: 1, 2].

## Circuit Diagram

![Circuit Diagram](led.png)[cite: 1]

## Hardware & Components

* **Microcontroller:** Arduino Uno
* **LEDs:** 1x Green LED, 1x Red LED, 1x Blue LED
* **Resistors:** 3x 200 $\Omega$ resistors (one per LED)
* **Prototyping:** Solderless breadboard and jumper wires[cite: 1]

## Pinout & Wiring

| Component | Arduino Pin | Notes |
| :--- | :--- | :--- |
| Green LED (via 200 $\Omega$ resistor) | Pin `13` | Anode (`+`) connected through resistor to pin `13` |
| Red LED (via 200 $\Omega$ resistor) | Pin `12` | Anode (`+`) connected through resistor to pin `12` |
| Blue LED (via 200 $\Omega$ resistor) | Pin `11` | Anode (`+`) connected through resistor to pin `11` |
| All LED Cathodes (`-`) | `GND` | Connected to a shared breadboard ground rail wired to Arduino `GND`[cite: 1] |

## How It Works

In `sketch.ino`, pins `13`, `12`, and `11` are configured as outputs in `setup()`[cite: 2]. Inside `loop()`, each LED turns `HIGH` for `300 ms`, turns `LOW`, and pauses for `50 ms` before the next LED in the sequence activates[cite: 2]:

1. **Pin `13` (Green):** `HIGH` for `300 ms` $\rightarrow$ `LOW` for `50 ms`[cite: 1, 2]
2. **Pin `12` (Red):** `HIGH` for `300 ms` $\rightarrow$ `LOW` for `50 ms`[cite: 1, 2]
3. **Pin `11` (Blue):** `HIGH` for `300 ms` $\rightarrow$ `LOW` for `50 ms`[cite: 1, 2]

## Getting Started

1. Place `led.png` in the root of your repository so the diagram displays properly.
2. Wire the circuit on your breadboard as shown in the diagram and pinout table[cite: 1].
3. Open `sketch.ino` in the Arduino IDE, select your **Arduino Uno** board and port, and click **Upload**[cite: 1, 2].
