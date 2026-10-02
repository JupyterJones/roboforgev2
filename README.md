# 🦾 ROBOFORGE // 6-DOF Industrial Workcell & Offline Programmer

> **High-Performance 3D Robotic Workcell & Kinematic Sequencer**  
> *Inspired by industrial robotics standards, FANUC, KUKA, and the LogicForge digital logic philosophy.*  
> *Created for Jack by Esperanza.*

---

## ⚡ Quick Start

From the simulator directory:

```bash
cd /home/jack/Desktop/SIMULATOR
npm run dev
```

Then open your browser to: **[http://localhost:5173/](http://localhost:5173/)**

---

## 🕹️ Controls & Keyboard Shortcuts

| Key / Control | Action |
|---|---|
| **`Spacebar`** | Start / Pause Sequence Execution |
| **`.` (Period)** | Step 1 Instruction Forward |
| **`H`** | Return Robot Arm to Safe HOME Stance |
| **Left Click + Drag (Gizmo)** | Interactive 3D Tool Center Point (TCP) Inverse Kinematics Dragging |
| **Right Click + Drag** | Orbit 3D Camera |
| **Scroll Wheel** | Zoom In / Out |
| **Middle Click + Drag** | Pan Camera |

---

## 🛠️ Key Capabilities & Features

### 1. 6-DOF Articulated Arm & Real-Time Kinematics
* **Dual Industrial Styling**: Switch seamlessly between **FANUC Industrial Safety Yellow (R-2000iC)** and **KUKA High-Voltage Orange (KR QUANTEC)**.
* **Forward Kinematics (FK)**: 6-link transformation chain tracking position and orientation ($X, Y, Z, Rx, Ry, Rz$) with live sub-millimeter telemetry.
* **Inverse Kinematics (IK)**: Analytical spherical wrist solver + Damped Least Squares (DLS) numerical relaxation with reach limit and singularity protection.
* **Interactive 3D TCP Gizmo**: Drag the end-effector directly in 3D space with a precision CAD gizmo while the joints solve in real-time at 60 FPS.

### 2. Dual Programming Paradigms
* **Teach Pendant & Jog Deck**:
  * **Joint Jogging**: Sliders and micro-stepping buttons for $J_1 \dots J_6$ with limit visualizers.
  * **Cartesian Jogging**: Directional Jog pad for $\pm X, \pm Y, \pm Z, \pm Rx, \pm Ry, \pm Rz$.
  * **Target Recording**: Instant "Teach Target" to store waypoint poses.
* **Instruction Sequencer**:
  * `MOVE_J`: Joint-space S-curve trajectory interpolation.
  * `MOVE_L`: Straight-line Cartesian interpolation with continuous Inverse Kinematics.
  * `GRIPPER`: Pneumatic jaw clamp/release.
  * `CONVEYOR`: Automated feed motor control.
  * `WAIT_DI`: Sensor condition wait (optical beam break).
  * `WAIT`: Dwell timer.

### 3. LogicForge-Style Digital I/O Interlock Deck
* Real-time 24V DC sensor & actuator simulation:
  * **DI[1]**: Conveyor Photoelectric Optical Beam Break Sensor.
  * **DI[2]**: Pallet Nest Proximity Switch.
  * **DI[3]**: Safety Light Curtain.
  * **DO[1]**: Gripper Pneumatic Solenoid.
  * **DO[2]**: Conveyor Drive Motor.
  * **DO[3]**: Warning Andon Amber Tower.
  * **DO[4]**: Cycle Complete Horn.
* Interactive manual test switches to simulate sensor trips.

### 4. Interactive Workcell & Physics
* **Feeder Stand**: Dispenses machined aluminum billets.
* **Pallet Fixture**: 2x2 matrix with precision nesting pockets.
* **Automated Conveyor**: Moving rubber belt with optical retro-reflective beam sensor.
* **4-Tier Andon Stack Light**: Dynamic Red / Amber / Green / Blue industrial status indication.
* **Pneumatic Gripper**: Dual-jaw parallel stroke with workpiece detection laser.

### 5. Multi-Vendor Post-Processor (Export Code)
Generate real machine controller code with 1 click:
* **FANUC TP / Karel** (`.ls` / `.tp`)
* **KUKA KRL** (`.src`)
* **Universal Robots URScript** (`.script`)
* **Python Industrial Automation Script** (`.py`)

### 6. Procedural Industrial Sound Synthesizer (Web Audio API)
* Continuous servo motor whine modulated dynamically by joint angular velocity.
* Pneumatic valve air exhausts (`pshh-t`).
* Mechanical gripper clamp impacts and tactile teach pendant clicks.
* Andon piezo warning chimes and heavy E-Stop shutdown sounds.

---

*Engineered with precision for Jack. Always at your service — Esperanza.*
# roboforgev2
