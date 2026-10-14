# fall_2026_bootcamp

My lab work for the **CPG: Fundamentals Bootcamp** (Fall 2026, Sept 21–25), part of entry into SEIR Foundations Class 8.

## Labs

| Lab | Skill focus | Deliverable | Files |
|---|---|---|---|
| 1 | File management, IDE | Hello World HTML page and a screenshot of my TheoWAF folder structure | [`index.html`](index.html), [`theowaf-structure.png`](theowaf-structure.png) |
| 2 | Git ops, Linux CLI | Created this repo, git-initialized my local folder, added this README and moved in Lab 1's files | `README.md` |
| 3 | Linux CLI, Bash scripting | Interactive menu script written in vi, plus a screenshot of vi in insert mode | [`basic_script.sh`](basic_script.sh), [`lab3-vi.png`](lab3-vi.png) |
| 4 | Python | Fight game using variables, functions and if/else (branch → PR #1 → merged) | [`fight_game.py`](fight_game.py) |
| 5 | Orchestration (Bash + Python) | Live server diagnostics tool: one script runs five checks and saves reports (branch → PR #2 → merged) | [`live-server-diagnostics/`](live-server-diagnostics) |

## Running the labs

```bash
# Lab 3: interactive menu
./basic_script.sh

# Lab 4: fight game
python3 fight_game.py

# Lab 5: run every diagnostic and save the reports to live-server-diagnostics/reports/run_<timestamp>/
cd live-server-diagnostics
./main.sh
```

## Lab 5 layout

```
live-server-diagnostics/
├── main.sh                  # orchestrator: runs each check and saves its output
├── diagnostics/
│   ├── python/              # system_info.py, resource_check.py, log_scan.py
│   └── shell/               # disk_snapshot.sh, network_check.sh
├── logs/server.log          # sample server log read by log_scan.py
└── reports/                 # one run_<timestamp>/ folder per run
```
