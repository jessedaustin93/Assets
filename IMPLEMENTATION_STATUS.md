# Agent Mesh — Live Implementation Status

Snapshot of what the working World view actually implements, so asset/design work
stays tied to the real app. Updated 2026-06-28.

App lives in the `agent-mesh` repo: hub at `hub/`, World view at
`hub/static/world.js`, structure in `hub/static/stations.json`, telemetry
collector at `telemetry/collector.py`. Deployed on T5810, tailnet-only via
Tailscale Serve.

## Navigation (implemented)

```
MAP  →  STATION  →  ROOM (nested)  →  PROGRAM OPERATIONS
                                      └→  AGENT TERMINAL
```

- **Map** — one station per machine in a ring; central Command core = operator;
  tailnet lanes; shuttles = real `/api/activity` messages (sender→recipient).
- **Station** — the machine's services as rooms; live agents in an OPS strip.
- **Room** — nests via `children[]` (e.g. Arr Stack → Sonarr/Radarr/…). A room
  with a `url` opens that service's web UI in a new browser tab.
- **Program operations** — a leaf program shows live state, latency, probe,
  runtime, path, URL, and explicit Web UI / Health Check / View Logs / Assign
  Agent / Restart controls. Agent-backed actions use an online agent on the
  owning machine. Health and logs are read-only; restart is confirmed and keeps
  privileged work behind the exact-command approval workflow. Its deployed
  tactical layout separates identity/purpose, real telemetry/routing, explicit
  health state, and the command deck while remaining responsive.
- **Inventory editing** — authenticated UI controls create top-level programs or
  nested children, edit metadata/type/state/probes, and remove inventory records
  after confirmation. The canonical runtime catalog persists atomically at
  `/data/stations.json`; removal never uninstalls software.
- **Terminal** — click an agent → its live `world/@agent` thread (read + send).
  The deployed terminal uses the tactical panel language with a framed transcript
  and responsive command controls; it remains plain DOM text for low-end hardware.

World also has an asset manifest loader with procedural fallbacks. Full,
reduced-motion, and low-power render modes are selectable and persisted locally.
The first eight-family/five-state station concept sheet is stored in
`concepts/concept_station_icons_v1.png` with an RGBA background-removed copy;
individual production crops are intentionally still pending quality review.

## Machines (stations) — keyed by agent-id suffix

Stations are keyed by the agent-id suffix (`hp`/`t5810`/`t3610`/`x1`), NOT the
reported hostname, so they join reliably to agents.

| Key | Label | Real role |
|---|---|---|
| `t5810` | T5810 · AI Flagship | hub host, GTX 1070, heavy compute, telemetry collector |
| `t3610` | T3610 · Media & Infra | Docker media/arr stack, GTX 970 |
| `hp` | HP ProBook 650-G2 | daily driver / control, Vaultwarden |
| `x1` | ROG Ally (X1) | Windows: Aeon, SnifferOps, Android dev |

## Real services discovered (2026-06-27, live-probed)

T3610 (Docker): Jellyfin :8096, Plex :32400, Sonarr :8989, Radarr :7878,
Lidarr :8686, Prowlarr :9696, LazyLibrarian :5299, Jellyseerr :5055,
Navidrome :4533, Calibre-Web :8083, qBittorrent :8080 (via gluetun VPN),
slskd :5030, FlareSolverr :8191. Media on `/mnt/jellymedia1·2`, `/mnt/music`,
`/mnt/nas-ssd`.

T5810: Agent Mesh Hub :8787, GPU Reactor (GTX 1070), `/srv/mesh-vault`;
planned Aeon Core + SnifferOps.

HP: Vaultwarden (tailscale-served), SnifferOps, Agent Mesh dev checkout.

X1: Aeon (`C:\dev\ai\aeon-v1`), SnifferOps, Android dev (no web telemetry yet).

## Telemetry (implemented, real — no fake status)

- Hub: `telemetry` table + `GET/POST /api/telemetry`.
- Collector: `telemetry/collector.py`, a stdlib systemd **user** service on T5810
  (`agent-mesh-telemetry.service`). Every 30s it reads `/api/stations`,
  TCP-probes every node with a `probe {host,port}` over the tailnet, gathers
  T5810 GPU/CPU/RAM, and POSTs results.
- World colours each room by live state: **up** (green + latency), **down** (red),
  **no telemetry** (amber), **planned** (dashed). Stations show `up/total`.

## stations.json schema (single source of truth)

```jsonc
"t3610": {
  "label": "T3610 · Media & Infra",
  "host": "t3610.tail6777bc.ts.net",
  "role": "...",
  "rooms": [
    { "id": "t3610.arr", "name": "Arr Stack", "type": "media",
      "children": [
        { "id": "t3610.sonarr", "name": "Sonarr", "type": "media",
          "probe": { "host": "t3610.tail6777bc.ts.net", "port": 8989 },
          "url": "http://t3610.tail6777bc.ts.net:8989", "note": "TV" }
      ] }
  ]
}
```

- `type` ∈ reactor | bridge | lab | media | cargo | vault | comms (drives theme).
- `probe` → monitored; `id` must be globally unique. `url` → opens web UI.
- `state` (live | structure | planned) is the authored fallback when no probe.

The authenticated World editor writes the persistent catalog through
`GET/PUT /api/stations`; the collector and UI consume that same document.

## Current deployment note

- Program operations and complete inventory editing are deployed on T5810.
- World, Station, and Program Operations appearance layouts are deployed through
  `world.js?v=18` (Agent Mesh commit `2c13245`).
- The tactical agent Terminal is deployed as `terminal.css?v=1` (Agent Mesh
  commit `b43ff25`).
- Generated the agent, background, icon, and prop concept sheets from the current
  prompt set. Validated and cropped 12 optimized WebP backgrounds and 20
  transparent WebP room props, recorded them in `metadata/assets.manifest.json`,
  and deployed them through the runtime manifest in Agent Mesh commit `46d4eec`.
  World uses the network/station/low-power backdrops and selects room props from
  real inventory metadata. Agent and icon sheets remain concept sources until
  clean per-cell production crops are validated.
- qBittorrent and LazyLibrarian were repaired on T3610 after the original snapshot.
