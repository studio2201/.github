<div align="center">

# 🌊 STUDIO 2201 // SYSTEMS & DESKTOP LAB

**Uncompromising software for Wayland desktops, GitHub CI/CD pipelines, and the modern web.**
*Zero subprocesses · Zero external crate bloat · Strictly &le; 256 LOC per file*

[![Website](https://img.shields.io/badge/Portal-studio2201.com-2f6f5e?style=for-the-badge&logo=safari)](https://studio2201.com)
[![GNOME Suite](https://img.shields.io/badge/GNOME%2045--50-6%20Wayland%20Extensions-0b6e87?style=for-the-badge&logo=gnome)](https://github.com/orgs/studio2201/repositories)
[![CI/CD Gate](https://img.shields.io/badge/CI%2FCD%20Actions-5%2F5%20Verified-2f6f5e?style=for-the-badge&logo=githubactions)](https://studio2201.com/agents)
[![Tuition Not Coffee](https://img.shields.io/badge/Sponsor-Tuition%2C%20Not%20Coffee%20%F0%9F%8E%93-2ec27e?style=for-the-badge)](https://ubermetroid.github.io/tuition-not-coffee)

[**🌐 Explore studio2201.com**](https://studio2201.com) · [**🧩 GNOME Desktop Suite**](#-01--gnome-shell-desktop-suite-wayland-4550) · [**🛡️ GitHub CI/CD Actions**](#-02--github-cicd-actions--supply-chain-security) · [**⚡ Webpages & Portals**](#-03--webpages-microsites--interactive-portals) · [**📜 Engineering Doctrine**](#-04--immutable-engineering-constitution)

</div>

---

## 🧩 01 · GNOME Shell Desktop Suite (Wayland 45–50)

The **Studio 2201 Ocean Desktop Suite** turns GNOME Shell 45–50 into a cohesive, keyboard-driven, Wayland-native workstation. Every extension runs **100% in-process** (zero external daemons or `GLib.spawn*` subprocesses), passes **`shexli` with 0 errors and 0 warnings**, and includes **One-Click Suite Color Sync** so changing your accent border in one extension themes your entire desktop at once.

| Extension | Role | UUID & Install Package | Highlights | Links |
| :--- | :--- | :--- | :--- | :---: |
| 🐙 [**Kelp**](https://github.com/studio2201/kelp) | **Auto-Tiler** | `kelp@studio2201.github.io` (`v2.2.0`) | **Octopus (2D Binary Grid)**, **Seahorse (1/2/3-Column Scroller)** & **Otter (Floating)** modes, window stacking, Hyprland navigation & active focus borders. | [🌐 Site](https://studio2201.github.io/kelp/) · [⬇ Release](https://github.com/studio2201/kelp/releases/latest) |
| 🪸 [**Reef**](https://github.com/studio2201/reef) | **Dock & Panel** | `reef@studio2201.github.io` (`v1.2.0`) | Wayland pressure barriers, **Kelp-friendly window-dodge intellihide**, scroll-wheel window/workspace cycling & pill/edge panel styling. | [🌐 Site](https://studio2201.github.io/reef/) · [⬇ Release](https://github.com/studio2201/reef/releases/latest) |
| 🌊 [**Tide**](https://github.com/studio2201/tide) | **App Launcher** | `tide@studio2201.github.io` (`v1.2.1`) | Instant `Super` & `Super+Enter` modal launcher with cross-workspace open-window search, fuzzy scoring & `Ctrl+1..9` quick launch badges. | [🌐 Site](https://studio2201.github.io/tide/) · [⬇ Release](https://github.com/studio2201/tide/releases/latest) |
| 🌺 [**Coral**](https://github.com/studio2201/coral) | **App Grid** | `coral@studio2201.github.io` (`v1.4.0`) | Alphabetical App Grid & **Smart Auto-Folder Organizer** that prevents overflow pages by grouping loose apps into labeled category folders. | [🌐 Site](https://studio2201.github.io/coral/) · [⬇ Release](https://github.com/studio2201/coral/releases/latest) |
| 🐚 [**Seabed**](https://github.com/studio2201/seabed) | **Desktop Icons** | `seabed@studio2201.github.io` (`v1.5.0`) | Renders `~/Desktop`, Home, Trash & mounted drives directly inside `Main.layoutManager._backgroundGroup` with native bidirectional drag-and-drop. | [🌐 Site](https://studio2201.github.io/seabed/) · [⬇ Release](https://github.com/studio2201/seabed/releases/latest) |
| 🐟 [**Shoal**](https://github.com/studio2201/shoal) | **System Tray** | `shoal@studio2201.github.io` (`v1.2.0`) | Wayland-native AppIndicator, KStatusNotifierItem (`SNI`), DBusMenu & legacy XWayland top-bar tray with real-time Clutter shader tinting. | [🌐 Site](https://studio2201.github.io/shoal/) · [⬇ Release](https://github.com/studio2201/shoal/releases/latest) |

```bash
# Quick install any Studio 2201 GNOME Shell extension:
gnome-extensions install --force <ext>@studio2201.github.io.shell-extension.zip
gnome-extensions enable <ext>@studio2201.github.io
```

---

## 🛡️ 02 · GitHub CI/CD Actions & Supply-Chain Security

Five fail-closed supply-chain & post-quantum security gates written in **pure `std::` Rust** (zero `crates.io` dependencies), orchestrated by [`studio2201/studio2201`](https://github.com/studio2201/studio2201) and [`studio2201/cli`](https://github.com/studio2201/cli).

| Tool | Question Answered | Repository | Verdict & Badge |
| :--- | :--- | :--- | :---: |
| ✂️ [**Snip**](https://github.com/studio2201/snip) | *Did the AI leak secrets, PII, or broken RLS in this diff?* | [`studio2201/snip`](https://github.com/studio2201/snip) | [![Vibe-Safe](https://img.shields.io/badge/snip-0%20secrets-2f6f5e?logo=shield)](https://studio2201.com/snip) |
| 👁️ [**Vigil**](https://github.com/studio2201/vigil) | *How much of our risk comes from abandoned dependencies?* | [`studio2201/vigil`](https://github.com/studio2201/vigil) | [![Dormancy](https://img.shields.io/badge/vigil-0%20dependencies-2f6f5e?logo=shield)](https://studio2201.com/vigil) |
| 🛡️ [**Aegis**](https://github.com/studio2201/aegis) | *Which RSA/ECC lines block our 2030 Post-Quantum migration?* | [`studio2201/aegis`](https://github.com/studio2201/aegis) | [![PQC](https://img.shields.io/badge/aegis-PQC%20compliant-2f6f5e?logo=shield)](https://studio2201.com/aegis) |
| 🔏 [**Proven**](https://github.com/studio2201/proven) | *Does this binary byte-match its ML-DSA-65 attested source?* | [`studio2201/proven`](https://github.com/studio2201/proven) | [![SLSA](https://img.shields.io/badge/proven-ML--DSA--65%20verified-2f6f5e?logo=shield)](https://studio2201.com/proven) |
| 🦴 [**Boneyard**](https://github.com/studio2201/boneyard) | *Which repositories in our org are quietly accumulating debt?* | [`studio2201/boneyard`](https://github.com/studio2201/boneyard) | [![Boneyard](https://img.shields.io/badge/boneyard-maintained-2f6f5e?logo=shield)](https://studio2201.com/boneyard) |
| 🧰 [**CLI**](https://github.com/studio2201/cli) & [**Canary**](https://github.com/studio2201/canary) | *Unified workstation CLI (`studio2201 check`) & negative failure testbed* | [`studio2201/cli`](https://github.com/studio2201/cli) | [![Toolchain](https://img.shields.io/badge/toolchain-unified-blue.svg)](https://studio2201.com) |

### 2-Second Workstation & GitHub Actions Setup

```bash
# Install the unified CLI and all five security tools into ~/.local/bin:
curl -fsSL https://studio2201.com/install.sh | sh -s all && studio2201 check
```

```yaml
# Drop-in GitHub Actions Gate (.github/workflows/security.yml):
- uses: studio2201/studio2201@v1
  with:
    tools: 'all'
    fail-on: 'block'
```

---

## ⚡ 03 · Webpages, Microsites & Interactive Portals

Every Studio 2201 project ships with a custom, zero-framework static web experience engineered for instant load times and strict **&le; 256 LOC** file discipline:

- 🌐 [**studio2201.com**](https://studio2201.com) ([`studio2201/studio2201.com`](https://github.com/studio2201/studio2201.com)) — Main organization storefront, [**AI Agent & MCP Guide**](https://studio2201.com/agents), and [**Canary Failure Breakdown**](https://studio2201.com/canary).
- 🌊 **Ocean Suite Microsites** — Glassmorphic product pages at [`studio2201.github.io/kelp`](https://studio2201.github.io/kelp/), [`/reef`](https://studio2201.github.io/reef/), [`/tide`](https://studio2201.github.io/tide/), [`/coral`](https://studio2201.github.io/coral/), [`/seabed`](https://studio2201.github.io/seabed/), and [`/shoal`](https://studio2201.github.io/shoal/).
- 🎓 [**Tuition, Not Coffee**](https://ubermetroid.github.io/tuition-not-coffee) — Community sponsorship page supporting our daughter's college tuition fund.

---

## 📜 04 · Immutable Engineering Constitution

1. **The Page Rule (16..=256 LOC)**: Every source file across all 16 repositories fits on a single human-auditable page (&le; 256 lines).
2. **Zero External Bloat**: Pure `std::` Rust in our CI/CD tools; zero external subprocesses or npm dependencies in our Wayland GNOME extensions.
3. **Fail-Closed Verification**: Automated CI gates (`shexli` 0-warning EGO review, headless GJS/GTK4 behavioral tests, and `canary` negative testbeds) guard every commit.
