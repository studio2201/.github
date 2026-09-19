# studio2201

[![studio2201 Suite](https://img.shields.io/badge/studio2201-5%2F5%20Verified-2f6f5e?logo=shield)](https://studio2201.com/agents#badges)
[![Website](https://img.shields.io/badge/website-studio2201.com-2f6f5e)](https://studio2201.com)
[![Parent Framework](https://img.shields.io/badge/framework-v1.3.4-blue.svg)](https://github.com/studio2201/studio2201)
[![License](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](LICENSE)

Software that exposes the true state of your systems. Pure `std::` Rust. Zero external dependencies. Strictly &le; 256 LOC per file.

<details open>
<summary><a href="https://studio2201.com/agents#badges"><img src="https://img.shields.io/badge/studio2201-5%2F5%20Verified-2f6f5e?logo=shield" alt="studio2201 Suite"></a> <b>Detailed Governance Scorecard</b></summary>

| Tool | Focus | Verdict | Status Badge |
| :--- | :--- | :---: | :---: |
| [**Snip**](https://github.com/studio2201/snip) | Vibe-Code & Secrets Gate | `SHIP` | [![Vibe-Safe](https://img.shields.io/badge/vibe--safe-SHIP-brightgreen.svg)](https://github.com/studio2201/snip) |
| [**Vigil**](https://github.com/studio2201/vigil) | Supply-Chain Dormancy | `HEALTHY` | [![Dormancy](https://img.shields.io/badge/dormancy-healthy-2f6f5e.svg)](https://github.com/studio2201/vigil) |
| [**Aegis**](https://github.com/studio2201/aegis) | PQC & Post-Quantum Scans | `QUANTUM-SAFE` | [![PQC](https://img.shields.io/badge/PQC-Quantum--Safe-blueviolet.svg)](https://github.com/studio2201/aegis) |
| [**Proven**](https://github.com/studio2201/proven) | ML-DSA-65 Attestation | `VERIFIED` | [![SLSA](https://img.shields.io/badge/SLSA-Level%203%2B-blue.svg)](https://github.com/studio2201/proven) |
| [**Boneyard**](https://github.com/studio2201/boneyard) | Tech-Debt Radar | `0/100 DEBT` | [![Boneyard](https://img.shields.io/badge/boneyard%20index-0%2F100-brightgreen.svg)](https://github.com/studio2201/boneyard) |

</details>

---

## The Six-Tool Security & Governance Suite

| Product | Focus | Repository | Description |
| :--- | :--- | :--- | :--- |
| **Snip** | Vibe-Code Security | [`studio2201/snip`](https://github.com/studio2201/snip) | Audits git diffs for live secrets, tokens, and SQL without Row Level Security. |
| **Vigil** | Supply-Chain Dormancy | [`studio2201/vigil`](https://github.com/studio2201/vigil) | Inspects package manifests and flags unmaintained/abandoned dependencies. |
| **Aegis** | Post-Quantum Migration | [`studio2201/aegis`](https://github.com/studio2201/aegis) | Scans codebases for classical crypto (RSA/ECC) breaching OMB M-26-15. |
| **Proven** | PQC-Signed Attestations | [`studio2201/proven`](https://github.com/studio2201/proven) | Generates SLSA L3+ in-toto attestations signed with pure `std::` ML-DSA-65. |
| **Boneyard** | Tech-Debt Radar | [`studio2201/boneyard`](https://github.com/studio2201/boneyard) | Aggregates repository health into a definitive 0–100 Boneyard Index. |
| **CLI** | Unified Toolchain | [`studio2201/cli`](https://github.com/studio2201/cli) | Manages all five tools and drives local pre-commit compliance audits. |
| **Canary** | Negative Testbed | [`studio2201/canary`](https://github.com/studio2201/canary) | Deliberately flawed reference repository asserting exit code 1 failures. |

---

## 2-Second Workstation Setup

Install the complete toolchain into `${XDG_BIN_HOME:-$HOME/.local/bin}`:

```bash
# Install the unified CLI and all five security tools
curl -fsSL https://studio2201.com/install.sh | sh -s all

# Run organization-wide compliance check on current repo
studio2201 check
```

---

## GitHub Actions CI Enforcement

Enforce all security gates on every pull request using the composite action:

```yaml
name: studio2201 Security Gate
on:
  pull_request:
    branches: [ master, main ]
  push:
    branches: [ master, main ]
permissions:
  contents: read
jobs:
  security-gate:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
        with:
          fetch-depth: 0
      - name: Run studio2201 Multi-Tool Gate
        uses: studio2201/studio2201@master
        with:
          tools: 'all'
          fail-on: 'block'
```

---

## Immutable Engineering Constitution

1. **Zero External Dependencies**: Pure `std::` Rust only — 0 crates from `crates.io`.
2. **The 256 LOC Rule**: Every file across all repositories is strictly &le; 256 LOC.
3. **Fail-Closed Tri-State**: `0` = Pass/Clean, `1` = Policy Block/Violation, `2` = CLI Error.
4. **Hostile Boundary Testing**: Verified against deliberate defect fixtures in `canary`.
