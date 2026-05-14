# echo1 pipeline simulator simulator 🚰

A fully client-side, browser-based hydraulic pipeline simulator designed for OT training, Human Factors Integration (HFI) research, and control room operator familiarization. 

*(Wait, why "simulator simulator"? Because true pipeline simulators use heavy Method of Characteristics (MOC) math to calculate real-time wave transients. Echo1 runs a sequential steady-state solver in a high-speed loop and fakes the fluid momentum using a dynamic time-delay buffer. It simulates being a simulator!)*

Unlike traditional simulators that require expensive backend servers, Echo1 compiles the industry-standard **EPANET** physics engine into WebAssembly (Wasm) to calculate real friction loss, flow rates, and gravity drafting natively in your browser.

### Core Features
* **Pseudo-Transient Hydraulic Math:** Driven by `epanet-js`, dynamically solving steady-state pressures and flows at 1-second intervals and buffering them to simulate the speed of sound.
* **Leak Detection System (LDS):** Built-in Computational Pipeline Monitoring (CPM) featuring 5-minute/1-hour rate deviation nets and a CUSUM volume balance.
* **API 1165 Compliant UI:** Designed using strict high-performance HMI standards (grayscale backgrounds, reserved alarm colors, proper typography hierarchy).
* **ISA 18.2 Alarm Symbology & Audio:** Multi-tiered alarm state management featuring a custom Web Audio API engine for authentic control room chimes.
* **Edge Emulation (BYOB):** Connect to your own MQTT broker to publish real-time station telemetry or subscribe to remote JSON commands (e.g., Emergency Shutdowns).

### Usage
Simply navigate to the live GitHub Pages link to run the simulator directly in your browser. No installation or backend required.

### About
Designed and maintained by **[Control Room Support Services](https://crss.ca)** (audits • risk • forensics • human factors integration).

### License
This project is licensed under the GNU Affero General Public License v3.0 (AGPL-3.0).
