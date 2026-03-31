<div align="center">
  
# 🏎️ Drive Mad

> **An intense, physics-based driving simulation that tests your precision and balance on treacherous tracks.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Platform: Web](https://img.shields.io/badge/Platform-Web-blue.svg)](#)

</div>

## 🎯 Overview

**Drive Mad** is not your typical racing game. It is a physics-driven obstacle course where every move matters. Whether you're navigating a narrow bridge or performing a high-speed jump, your success depends on managing your vehicle's center of gravity and engine power.

The game uses a complex physics engine compiled for the web, providing a console-quality experience in a lightweight, browser-native format.

---

## 🚀 Key Features

*   **🛡️ Realistic Physics Engine**: Experience authentic weight distribution and suspension modeling.
*   **🛣️ Creative Level Designs**: Levels range from simple speed traps to mind-bending stunts and loops.
*   **📦 No Installation**: Runs on **WebAssembly (WASM)** for near-native performance without any plugins.
*   **📱 Responsive & Accessible**: Automatically adapts to Desktop (Keyboard) and Mobile (Touch) controls.

---

## 🎮 Game Mechanics Explained

To succeed in **Drive Mad**, you must master three core areas:

1.  **Weight Shift Management**: When jumping, use forward/backward inputs to level the vehicle. Landing flat is the only way to avoid the explosive "crashes" that reset your progress.
2.  **Momentum vs. Speed**: Higher speed doesn't always help. Many levels require you to *decelerate* mid-air or take ramps at precise speeds to clear specific gaps.
3.  **Traction Control**: The surface in each level affects your grip. Look for visual cues in the environment to know when to floor the pedal and when to feather it.

### Controls

| Action            | Keyboard / Mouse                                              |
| :---------------- | :------------------------------------------------------------ |
| **Drive Forward** | `W`, `D`, `X`, `Up Arrow`, `Right Arrow`, `Left Mouse Button` |
| **Drive Backward**| `S`, `A`, `Z`, `Down Arrow`, `Left Arrow`                     |

---

## 🛠️ Technical Deep-Dive

This project demonstrates the power of modern web standards:

### ⚙️ Why WebAssembly (Wasm)?
The core game engine is written in C++ for maximum performance. Traditional JavaScript engines can struggle with complex physics calculations at 60FPS. By using **Emscripten** to transpile the game to **WebAssembly**, we achieve:
- **Consistent Frame Rate**: Reduced garbage collection pauses.
- **Native Efficiency**: Near-native execution speeds for the physics simulation.
- **Compact Delivery**: Smaller binary sizes compared to bulky JavaScript bundles.

### 🖼️ Graphics & UI
- **HTML5 Canvas**: The primary rendering target for the high-performance graphics.
- **Responsive Wrappers**: The UI dynamically scales using CSS and JS, ensuring the game occupies the optimal screen space on any device.

### 🍱 Integrated SDKs
- **Poki SDK**: Seamlessly integrates with the Poki platform for loading states, analytics, and game life-cycle management.

---

## 📂 Project Structure

- `index.html`: The main entry point, housing the Emscripten loader and game UI.
- `webapp/`: Contains game assets, including textures like `cover.jpg`.
- `wasm/`: (Internal) The compiled WebAssembly module and its JavaScript bridge.

---

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

*Enjoy the ride, master the physics, and try not to drive mad!*

