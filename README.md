# 🎯 Angry Birds – FPGA Game (SystemVerilog, VGA Engine)

A fully hardware-based Angry Birds–style game implemented in **SystemVerilog**, designed and built for an FPGA with real-time VGA graphics, keyboard input, physics-based motion, and multiple interactive game objects.

This project was created as part of the Technion Winter 2025 Digital Systems Laboratory.

---

## 📘 Project Presentation  
👉 **[View the full PDF presentation](docs/.pdf)**

The presentation includes system architecture, hierarchy diagrams, model descriptions, gameplay screenshots, block diagrams, and signal traces.

---

## 🧩 Project Description

The game simulates the classic Angry Birds mechanics:

- The bird launches at different **angles** and **strengths** depending on how far it is pulled back.
- Pigs appear in multiple variations:
  - Normal pig  
  - Helmet pig (takes multiple hits)  
  - King pig  
  - Teleporting pig (moves position twice upon damage)
- A **moving tree** adds dynamic obstacles.
- Wooden/stone blocks form structures around pigs.
- Player wins after eliminating all pigs — a custom **victory screen** appears.

*Reference: Project characterization on page 3 of the PDF.* :contentReference[oaicite:1]{index=1}

---

## 🕹️ System Interfaces

The system uses:
- **Keyboard input** → bird control & tension management  
- **FPGA logic** → object rendering, motion physics, collision detection  
- **VGA output** → real-time graphical display  
- **Audio unit** → sound effects (win screen, impacts)

*See the system interface diagram on page 4.* :contentReference[oaicite:2]{index=2}

---

## 🖼️ Screenshots of Gameplay

The game includes:
- Shooting view  
- Birds hitting pigs  
- Destructible block structures  
- Win screen after 10 kills  

*(Screenshots: page 5).* :contentReference[oaicite:3]{index=3}

---

## 🧭 Operating Instructions

- **Pull back** → bird tension increases  
- **Release** → bird launches  
- Movement keys adjust the bird’s stretch angle  
- Tension displayed visually during pull-back

*(Operating instructions: page 6).* :contentReference[oaicite:4]{index=4}

---

## 🧱 Architecture

### 🔷 Rectangle Scheme  
Main modules:
- Bird  
- Pig types  
- Obstacles  
- Blocks (wood/stone)  
- Tree  
- Keyboard interface  
- Game messages  
- Game controller  

*(Diagram: page 7).* :contentReference[oaicite:5]{index=5}

---

### 🏗️ Upper Hierarchy

The design is divided into multiple major hardware blocks:

- **Background engine**
- **Moving tree unit**
- **Kills counter**
- **Keyboard + Bird movement unit**
- **Game controller + mux**
- **Sound unit**
- **Numbers bitmap / on-screen digits**
- **Victory animation**

*(Hierarchies on pages 8–10).* :contentReference[oaicite:6]{index=6}

---

## 🦅 Model 1 – Bird Engine

Includes:
- **Bird Move**: FSM controlling movement, launch force, angles  
- **Square_Object**: defines rendering bounds  
- **Bird Bitmap**: draws the bird sprite  

Features:
- Collision with screen boundaries  
- Angle-based launch  
- Real-time bird trajectory  

*(Pages 11–12).* :contentReference[oaicite:7]{index=7}

---

## 🐷 Model 2 – Pigs & Blocks Engine

Handles:
- Pig health (normal, helmet, king)
- Teleporting pig logic  
- Block destruction states  
- Objects matrix rendering (16×16 grid)
- Bitmap selection per object type

Block size: **32×32 px**  
Matrix resolution used: **512×416** inside VGA canvas

*(Pages 13–14).* :contentReference[oaicite:8]{index=8}

---

## 📊 Signal Trace (Kills Counter)

The kills counter increments **only when a pig dies**, and the win signal triggers exactly on the **10th kill**.

*(Signal tab: page 15).* :contentReference[oaicite:9]{index=9}

---

## ✅ Summary & Conclusions

- Learned to break a large system into modular hardware units  
- Gained deep experience with **SystemVerilog**, VGA rendering, FSMs, and game logic  
- Improved teamwork, model organization, and top-down hardware design  
- Produced a fully working FPGA game with real-time animation and physics  

*(Page 16).* :contentReference[oaicite:10]{index=10}

---

## 🛠️ Technologies Used

- SystemVerilog  
- Quartus Prime  
- FPGA board (DE10 / similar)  
- VGA Controller  
- Finite State Machines  
- Hardware sprite rendering  
- Audio synthesis

---

## 👤 Authors
- **Hanna Ashkar**  
- **Jawad Semaan**

Instructor: Alon  
Winter 2025  
