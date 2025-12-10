#🎯 Angry Birds – FPGA Game (VGA)
A hardware-accelerated Angry Birds-style game built fully in Verilog, running on an FPGA board with VGA output, collision detection, physics logic, and interactive controls.
✨ Features
VGA graphics engine (640×480 or 800×600)
Bird trajectory physics (parabolic motion)
Collision detection with blocks
Game state machine + score counter
Button/keyboard input for aiming & firing
Hardware-based real-time rendering
📘 Presentation
👉 View full project presentation (PDF)
🏗️ Project Architecture
vga_controller.v – handles VGA sync signals & pixel scanning
physics.v – motion equations & gravity
collisions.v – hit detection
game_state.v – finite state machine
top.v – integrates all modules
🛠️ Tools & Technologies
Verilog HDL
Quartus Prime
DE1 / DE10 / FPGA board
ModelSim simulation
VGA driver implementation

🧑‍💻 Author
Hanna Ashkar — Electrical Engineering, Technion
FPGA, Computer Architecture, Digital Systems
