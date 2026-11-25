<p align="center"><img src="assets/banner.svg" width="100%" alt="Trịnh Nhựt Phát — Robotics · Mobile Robots & UAVs · Embedded Rust"/></p>

<p align="center">
  <a href="mailto:phatsuper14785@gmail.com"><img src="https://img.shields.io/badge/Email-phatsuper14785%40gmail.com-0f1729?style=for-the-badge&logo=gmail&logoColor=34d6b0&labelColor=0a0f1c" alt="Email"/></a>
  <img src="https://img.shields.io/badge/RAI_Lab-HCMUTE-0f1729?style=for-the-badge&labelColor=0a0f1c&color=0f1729" alt="RAI Lab HCMUTE"/>
  <img src="https://img.shields.io/badge/Open_to-Robotics_internships-ffb347?style=for-the-badge&labelColor=0a0f1c" alt="Open to internships"/>
</p>

I build **robots**, from warehouse AMRs to quadrotors, in simulation first, then the low-level software that has to run on them reliably. Most of my projects ship with a **reproducible check and a number**: an RMSE against ground truth, a latency percentile, or a crash-recovery test.

## `$ whoami`

<p align="center"><img src="assets/whoami.svg" width="100%" alt="whoami: Trịnh Nhựt Phát, RAI Lab HCMUTE, Robotics & AI, UAV autonomy, safe RL, embedded Rust"/></p>

## 🧭 Engineering focus

<p align="center"><img src="assets/focus.svg" width="100%" alt="Five layers: learning, robotics, flight stack, systems, bare metal"/></p>

## 🛠️ Tech stack

<p align="center"><img src="https://skillicons.dev/icons?i=rust,python,cpp,c,ts,ros,pytorch,linux,ubuntu,react,sqlite,git&theme=dark" alt="Rust, Python, C++, C, TypeScript, ROS, PyTorch, Linux, Ubuntu, React, SQLite, Git"/></p>

| Area | Tools |
|---|---|
| **Robotics & autonomy** | ROS 2 Jazzy, Nav2, SLAM Toolbox, Gazebo Harmonic, PX4 (SITL, MAVLink), PyTorch, PPO, Kalman / EKF |
| **Systems** | Rust (`no_std`, Tokio, Axum), C++, Python, FastAPI, MQTT |
| **Embedded / IoT** | UART framing & CRC, GPIO state machines, ESP32 + WebSocket |
| **Also** | MATLAB (quadrotor control), TypeScript / React, Linux, Git |

## 🚀 Selected work

<table>
<tr>
<td width="50%"><a href="https://github.com/David-Trinh-05/perchpilot"><img src="assets/perchpilot.svg" width="100%" alt="PerchPilot"/></a></td>
<td width="50%"><a href="https://github.com/David-Trinh-05/aisleops-amr"><img src="assets/aisleops.svg" width="100%" alt="AisleOps AMR"/></a></td>
</tr>
<tr>
<td width="50%"><a href="https://github.com/David-Trinh-05/swarm-dashboard-cbf-rl"><img src="assets/swarm.svg" width="100%" alt="Swarm Dashboard"/></a></td>
<td width="50%"><a href="https://github.com/David-Trinh-05/mini-kv-store"><img src="assets/kvstore.svg" width="100%" alt="mini-kv-store"/></a></td>
</tr>
</table>

<a href="https://github.com/David-Trinh-05/perchpilot"><img src="assets/perch-arch.svg" width="100%" alt="PerchPilot architecture: GPU simulator, PPO, weight export, Rust perch_core, PX4 SITL, Gazebo HoldPad, attachment verifier"/></a>

<details>
<summary><b>Smaller Rust tools</b>: telemetry, embedded, CLI</summary>

| Repo | What it proves |
|---|---|
| [telemetry-ingest](https://github.com/David-Trinh-05/telemetry-ingest) | Returns HTTP 503 under backpressure; on SIGTERM drains all 2,112 admitted records in order |
| [telemetry-frame](https://github.com/David-Trinh-05/telemetry-frame) | `no_std`, zero-dependency UART framing + CRC-16; builds for `thumbv6m-none-eabi` |
| [button-debounce](https://github.com/David-Trinh-05/button-debounce) | Non-blocking GPIO debounce state machine for bare-metal |
| [http-pulse](https://github.com/David-Trinh-05/http-pulse) | Bounded concurrent HTTP health checks for deploy pipelines |
| [telemetry-replay](https://github.com/David-Trinh-05/telemetry-replay) | Replays timestamped sensor logs at adjustable speed |

</details>

## 📐 How I work

| | Principle | Where you can see it |
|---|---|---|
| 🛑 | **Gate before you actuate.** Nothing powers down or takes control until a check passes. | PerchPilot verifies attachment before motors-off · Swarm keeps OFFBOARD inactive behind readiness gates |
| 📏 | **Measure against ground truth.** A demo without a number is a video. | AisleOps scores AMCL at 5.0 cm RMSE against Gazebo pose |
| 💥 | **Assume the crash.** Kill it mid-write and check what survives. | mini-kv-store SIGKILL recovery · telemetry-ingest ordered drain on SIGTERM |
| 🔁 | **Port it and prove parity.** | PerchPilot's Python policy node rewritten in Rust: output parity ≤ 5e-6 |

## 📓 Flight log

- [x] Rewrote PerchPilot's onboard node in Rust (`r2r`), matching the Python node to 5e-6
- [x] Replaced learned depth in the swarm follow-target with bearing-only multi-view EKF
- [x] Nav2 delivery mission on a saved SLAM map, scored against Gazebo ground truth
- [ ] Move from SITL to hardware-in-the-loop for the perching stack
- [ ] Run `telemetry-frame` on a real MCU over UART

<p align="center"><img src="assets/footer.svg" width="100%" alt="End of log: Simulate it. Verify it. Then fly it."/></p>
