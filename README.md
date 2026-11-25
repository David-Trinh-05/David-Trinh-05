<p align="center"><img src="assets/banner.svg" width="100%" alt="Trịnh Nhựt Phát — Robotics & Embedded Software · UAV Autonomy · Rust"/></p>

I build robots and drones in simulation first, then the low-level software that has to run on them reliably. Most of my projects ship with a **reproducible check and a number**: an RMSE against ground truth, a latency percentile, or a crash-recovery test.

**Student @ HCMUTE** · Open to internships in **robotics, UAV autonomy and embedded / Rust software**<br/>
📫 [phatsuper14785@gmail.com](mailto:phatsuper14785@gmail.com)
<!-- Add when ready:  · [LinkedIn](https://linkedin.com/in/...) · [CV (PDF)](...) -->

## Selected work

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

## How I work

| | Principle | Where you can see it |
|---|---|---|
| 🛑 | **Gate before you actuate.** Nothing powers down or takes control until a check passes. | PerchPilot verifies attachment before motors-off · Swarm keeps OFFBOARD inactive behind readiness gates |
| 📏 | **Measure against ground truth.** A demo without a number is a video. | AisleOps scores AMCL at 5.0 cm RMSE against Gazebo pose |
| 💥 | **Assume the crash.** Kill it mid-write and check what survives. | mini-kv-store SIGKILL recovery · telemetry-ingest ordered drain on SIGTERM |
| 🔁 | **Port it and prove parity.** | PerchPilot's Python policy node rewritten in Rust: output parity ≤ 5e-6 |

## Toolbox

| Area | Tools |
|---|---|
| **Autonomy** | PX4 (SITL, MAVLink), ROS 2 Jazzy, Nav2, Gazebo Harmonic, PyTorch, PPO, Kalman / EKF |
| **Systems** | Rust (`no_std`, Tokio, Axum), C++, Python, FastAPI, MQTT |
| **Embedded / IoT** | UART framing & CRC, GPIO state machines, ESP32 + WebSocket |
| **Also** | MATLAB (quadrotor control), TypeScript / React, Linux, Git |
