🟣 PDA Visualizer
A sleek, interactive web-based simulator for Pushdown Automata (PDA). This tool allows users to define transitions, track stack operations in real-time, and visualize how a PDA processes an input string step-by-step.

🔗 Live Demo: https://shubhip27.github.io/PDA-simulator-/

✨ Features
Real-time Stack Visualization: Watch the stack grow and shrink with smooth animations as symbols are pushed and popped.
Step-by-Step Execution: Control the simulation at your own pace to debug complex transitions.
Custom Transition Logic: Define your own PDA using a simple, readable syntax.
Detailed Execution Log: A console-style history of every state change and stack operation.
Modern Lavender UI: Built with a glassmorphic aesthetic, featuring a responsive and clean layout.

🚀 Getting Started
1. Define Transitions
   Input your transitions in the sidebar using the following format:
   Current State, Input Char, Pop Symbol -> Next State, Push Symbols
   Use ε for empty moves (epsilon).
   Example for aⁿbⁿ :
  q0, a, Z -> q0, AZ
  q0, a, A -> q0, AA
  q0, b, A -> q1, ε
  q1, b, A -> q1, ε
  q1, ε, Z -> qf, Z

2. Initialize
   Set your Input String (e.g., aabb) and your Initial Stack Symbol (usually Z), then click INITIALIZE.
4. Step Through
   Click STEP FORWARD to process the string one character at a time. The visualizer will highlight the current state and the current state of the stack.

🛠️ Technical Stack
HTML5/CSS3: Custom CSS variables and Flexbox/Grid for a modern, responsive layout.
JavaScript (ES6): Logic for the state machine, transition parsing, and DOM manipulation.
Animations: CSS @keyframes for smooth stack transitions.

📝 Transition Syntax Guide
<img width="870" height="321" alt="image" src="https://github.com/user-attachments/assets/c91d3f07-7ed9-4bb1-9101-103caa72ed3c" />
