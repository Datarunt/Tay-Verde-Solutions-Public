## Edge Reliability: System Context

This repository is part of a larger **reliability-first industrial IoT system**.
The system is intentionally split into four focused, frozen repositories.

**Explore the full system:**
1. [Edge-reliability](https://github.com/Datarunt/Tay-Verde-Solutions-Edge-Reliability)
2. [Data-ingestion](https://github.com/Datarunt/Tay-Verde-Solutions-Data-Ingestion)
3. [Control-plane](https://github.com/Datarunt/Tay-Verde-Solutions-Control-Plane)
4. [ML-system](https://github.com/Datarunt/Tay-Verde-Solutions-ML-System)

- Hardware BOM (minimal)
- Wiring diagram photo (even if simple)
- How to flash/build
- Where logs live
- The failure injection checklist (brownout, disconnect, bus lock)
- Links to evidence in /docs/

Deliverables

- Boot reason logging
- Uptime counter
- Brownout logs (including forced brownout)
- Watchdog-safe main loop
- Sensor presence checks
- I²C recovery logic + measured recovery time
- Local persistence test notes
- Failure photos + diagnosis notes mapped to IPC-A-610

---

**Next:** See how edge data is validated and made replayable → [Data-ingestion](https://github.com/Datarunt/Tay-Verde-Solutions-Data-Ingestion)

