# 🟣 PDA Visualizer 

A sleek, interactive web-based simulator for **Pushdown Automata (PDA)**. This tool allows users to define transitions, track stack operations in real-time, and visualize how a PDA processes an input string step-by-step with a modern, glassmorphic UI.

🔗 **Live Demo:** https://shubhip27.github.io/PDA-simulator-/

---

## ✨ Features

* **Real-time Stack Visualization:** A vertical chamber that grows and shrinks with "bounce-in" animations as symbols are pushed or popped.
* **Step-by-Step Execution:** Manually trigger each transition to observe state changes and stack manipulations.
* **Custom Transition Logic:** Define any Deterministic PDA using a simple, readable string format.
* **Lavender Aesthetic:** A clean, student-friendly design featuring a violet/lavender color palette and backdrop-filter blurring.
* **Live Execution Log:** A scrollable console that tracks every successful transition or rejection error.

---

## 🚀 How to Use

### 1. Define Transitions
Input your rules in the text area using the following syntax:  
`Current State, Input Char, Pop Symbol -> Next State, Push Symbols`

* **Epsilon (ε):** Use `ε` for moves that don't consume input or for popping without pushing.
* **Example for $a^nb^n$:**
    ```text
    q0, a, Z -> q0, AZ
    q0, a, A -> q0, AA
    q0, b, A -> q1, ε
    q1, b, A -> q1, ε
    q1, ε, Z -> qf, Z
    ```

### 2. Initialization
* Enter your **Input String** (e.g., `aabb`).
* Set your **Initial Stack Symbol** (defaults to `Z`).
* Click **INITIALIZE** to reset the machine.

### 3. Simulation
* Click **STEP FORWARD** to process the string. 
* The **Status HUD** will update the current state and remaining input.
* The **Execution Log** will notify you if the string is **ACCEPTED** or **REJECTED**.

---

## 🛠️ Technical Overview

* **Frontend:** HTML5 & CSS3 (Grid/Flexbox, Custom Properties).
* **Logic:** JavaScript (ES6) state machine implementation.
* **UI/UX:** Glassmorphism, CSS `@keyframes` for stack items, and responsive design.

---

## 📝 Transition Syntax Guide

| Component | Description | Example |
| :--- | :--- | :--- |
| **State** | The current or next identifier | `q0`, `q1`, `qf` |
| **Input** | Char to consume (or `ε`) | `a`, `b`, `ε` |
| **Pop** | Symbol to match on top of stack | `Z`, `A` |
| **Push** | Symbols to add (use `ε` to pop only) | `AA`, `AZ`, `ε` |

---

