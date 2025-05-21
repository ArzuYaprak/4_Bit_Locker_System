![Image](https://github.com/user-attachments/assets/12ea5f2d-4b86-48da-8c9b-0cb3fba9ac06)
# 🔐 Digital Locker System - CircuitVerse

This project implements a *4-bit digital locker system* using a logic circuit simulator (CircuitVerse). The system validates password entries, tracks incorrect attempts, and provides visual feedback using LEDs and a 7-segment display.

---

## 🧠 Project Overview

The locker system includes:

- *4-bit password input* (via switches)
- *Password comparison logic*
- *Error counting with a 2-bit counter*
- *Three types of LED indicators*:
  - ✅ *Correct password* → Unlock LED (gray turns on)
  - ❌ *Incorrect password* → Error LED (red turns on)
  - 🔒 *Locked state* → Blue LED lights up after 3 wrong attempts
- *7-segment display* showing the number of attempts remaining: 3 → 2 → 1 → 0

---

## ⚙ How It Works

### 1. Password Comparison
- STORED INPUT: 4-bit preset password (default: 1011)
- USER INPUT: User enters a 4-bit value
- XOR gates compare each bit; if all are equal, the Correct LED turns ON.
- If incorrect, the False LED lights up.

### 2. Error Tracking
- Every incorrect attempt *increments the 2-bit counter*.
- The counter's value is *inverted* (3 becomes 0, 2 becomes 1...) and passed to a 7-segment display labeled "Attempts Remaining".

### 3. Lock Mechanism
- When the counter reaches 3:
  - Clocked LED turns ON (blue LED).
  - Further inputs are ignored until a *manual Reset* is pressed.

---

## 🖥 Components Used

| Component          | Description                            |
|-------------------|----------------------------------------|
| 4-bit XOR gates    | Password bit comparison                |
| AND, NOT gates     | Logic control for output signals       |
| Counter (2-bit)    | Tracks incorrect attempts              |
| 7-segment display  | Shows remaining attempts               |
| 3 LEDs             | For Correct, False, and Locked states  |
| Buttons & Switches | For Enter and Reset actions            |
| Splitters          | Separates counter output for display   |

---

## ✅ How to Use

1. Set your *4-bit stored password* using the switches labeled STORED INPUT.
2. Enter a guess via the USER INPUT switches.
3. Press the *ENTER* button:
   - If correct → *Gray LED* lights up, no counter increment.
   - If incorrect → *Red LED* lights up, counter increases.
4. On the 3rd incorrect attempt:
   - *Blue LED* turns ON.
   - System is LOCKED.
5. To reset:
   - Press the *RESET* button.

---

## 📷 Preview

![System Layout](circuit_diagram.png)

---

## 📁 Files

- CircuitVerse project: contains the full logic circuit.
- README.md: this explanation file.
- Optional: Screenshots or GIFs showing usage.

---

## 🧑‍💻 Developer

This project was implemented by *[Your Name]* as part of the final assignment for the *Digital Logic Circuit Design* course at *Istanbul Health and Technology University*.

---
