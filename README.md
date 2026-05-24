# BBLogger

**Flight log collection utility for BlueBird Aero Systems.**

BBLogger guides the operator through a step-by-step wizard to collect and organize flight logs from multiple sources — SD cards, SSD (WALDO), GCS logs, MUX/OBS recordings, Event Viewer, and more — into a single structured output folder per mission.

---

## Download

👉 **[Download BBLogger.exe](https://github.com/itaylevi1302/BBLogger-releases/releases/latest/download/BBLogger.exe)**

[View all releases](https://github.com/itaylevi1302/BBLogger-releases/releases)

> Windows only · Run as Administrator (UAC prompt appears on first launch)

---

## System Requirements

| Requirement | Details |
|---|---|
| OS | Windows 10 / 11 |
| Privileges | Administrator (auto-elevated via UAC) |
| Storage | ~50 MB for the application |

No Python installation required — the release is a standalone `.exe`.

---

## How to Use

1. **Launch** `BBLogger.exe` as Administrator (or accept the UAC prompt).
2. **Select dates** — pick one or two consecutive flight dates.
3. **Clock status** — confirm whether the PC clock is synchronized (informational only; does not block retrieval).
4. **Choose retrieval mode** — Full Day (all logs for the date) or Per-Flight (define exact sortie time windows).
5. **Enter tail number** — English letters and digits only.
6. **Select aircraft version and components** — choose which log sources to collect.
7. **Enter a description** — short label used in the output folder name (e.g. `TEST-FLIGHT`, `GIMBAL-ERROR`).
8. **Review the summary** and click **Start Copy**.
9. When prompted, insert the **AP / FMC SD card** or **WALDO SSD**.
10. When complete, click **Open Folder** to open the mission folder.

---

## Output Structure

```
C:/BBLOGGER/Logs/
  └── <DATES> - <AIRCRAFT> - <TAIL> - <DESCRIPTION>/
        ├── AP/
        ├── FMC/
        ├── WALDO/
        ├── BBGCS/
        ├── MUX/
        ├── OBS/
        ├── MISSION/
        ├── SOLO/
        ├── Event Viewer/
        └── SpyxUavLogs/
```

In **Per-Flight** mode, a subfolder is created per sortie under the mission folder.

---

## Configuration

User-editable paths are stored at `C:/BBLOGGER/bblogger_paths.json` and can be modified via the **Settings** button on the first screen.

---

## Support

For issues or questions, contact the **BlueBird Aero Systems Technical Department**.

Session logs are saved at `C:/BBLOGGER/AppFailLogs/BBLogger_Log_<date>.txt`.

---

*BBLogger v2.3.1 · BlueBird Aero Systems · Technical Department*
