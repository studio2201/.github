# studio2201 default ports

Canonical listen ports for all apps. **No collisions.**

## Web services — `4401`–`4410`

| Port | App | Notes |
|-----:|-----|--------|
| **4401** | [beam](https://github.com/studio2201/beam) | File sharing |
| **4402** | [pad](https://github.com/studio2201/pad) | Collaborative scratchpad |
| **4403** | [todo](https://github.com/studio2201/todo) | Task lists |
| **4404** | [trace](https://github.com/studio2201/trace) | Network / WHOIS / ASN |
| **4405** | [grid](https://github.com/studio2201/grid) | Kanban |
| **4406** | [pulse](https://github.com/studio2201/pulse) | System metrics |
| **4407** | [statesync](https://github.com/studio2201/statesync) | Emby ↔ Jellyfin sync dashboard |
| 4408–4410 | *(reserved)* | |

## Web games — `4501`–`4510`

| Port | App | Notes |
|-----:|-----|--------|
| **4501** | [snake](https://github.com/studio2201/snake) | Snake |
| **4502** | [rustle](https://github.com/studio2201/rustle) | Wordle clone |
| **4503** | [scan](https://github.com/studio2201/scan) | Sector scanner / minesweeper |
| **4504** | [defend](https://github.com/studio2201/defend) | Space shooter |
| 4505–4510 | *(reserved)* | |

## Rules

1. **Container `EXPOSE` / `ENV PORT`** and **host `-p`** use the same number by default (`-p 4401:4401`).
2. **Unraid templates**, **docker-compose**, **`.env.example`**, and **README** must match this table.
3. Override with `PORT` (or `STATESYNC_BIND` / `TRACE_PORT` where used) when needed.
4. **Do not** repurpose Emby/Jellyfin examples on **8096** — that is media-server port, not StateSync’s listen port.

Last aligned: 2026-07-27.
