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
| **4407** | [habit](https://github.com/studio2201/habit) | Habit tracker / streaks *(planned)* |
| **4408** | [mark](https://github.com/studio2201/mark) | Bookmarks |
| **4409** | [poll](https://github.com/studio2201/poll) | Polls / quick votes *(planned)* |
| **4410** | [probe](https://github.com/studio2201/probe) | Uptime / endpoint health *(planned)* |

## Web games — `4501`–`4510`

| Port | App | Notes |
|-----:|-----|--------|
| **4501** | [snake](https://github.com/studio2201/snake) | Snake |
| **4502** | [rustle](https://github.com/studio2201/rustle) | Wordle clone |
| **4503** | [scan](https://github.com/studio2201/scan) | Sector scanner / minesweeper |
| **4504** | [defend](https://github.com/studio2201/defend) | Space shooter |
| 4505–4510 | *(reserved)* | |

## Media services — `4601`–`4610`

Media-stack sidecars and dashboards (not general web apps; not games).

| Port | App | Notes |
|-----:|-----|--------|
| **4601** | [statesync](https://github.com/studio2201/statesync) | Emby ↔ Jellyfin watch-state sync dashboard |
| 4602–4610 | *(reserved)* | |

## Rules

1. **Container `EXPOSE` / `ENV PORT`** and **host `-p`** use the same number by default (`-p 4401:4401`, `-p 4601:4601`).
2. **Unraid templates**, **docker-compose**, **`.env.example`**, and **README** must match this table.
3. Override with `PORT` (or `STATESYNC_BIND` / `TRACE_PORT` where used) when needed.
4. **Do not** repurpose Emby/Jellyfin examples on **8096** — that is the media server’s own port, not StateSync’s listen port.

Last aligned: 2026-07-28 (habit / mark / poll / probe claimed on 4407–4410).
