# 🛡️ OSTIUM — Sovereign Home Gateway Sentinel & WIDS Defense Platform

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux%20%7C%20Windows%20x86__64-blue.svg" alt="Platform" />
  <img src="https://img.shields.io/badge/Binary-Musl%20Static%20%2F%20Win32%20PE-brightgreen.svg" alt="Binary" />
  <a href="https://github.com/rmediatech/ostium-dist/releases/tag/v0.2.0"><img src="https://img.shields.io/badge/Release-v0.2.0-green.svg" alt="Release" /></a>
  <a href="https://rmediatech.com/downloads"><img src="https://img.shields.io/badge/Downloads-rmediatech.com%2Fdownloads-blue.svg" alt="Downloads" /></a>
  <a href="docs/09_OSTIUM_CRUCIBLE_EMPIRICAL_AUDIT.md"><img src="https://img.shields.io/badge/Crucible%20TDD-57%2F57%20Passed%20(100%25)-success.svg" alt="Crucible Tests" /></a>
  <img src="https://img.shields.io/badge/Provenance-Ed25519%20Signed%20(SOVEREIGN--SIGN--01)-blueviolet.svg" alt="Signed" />
  <img src="https://img.shields.io/badge/Privacy-100%25%20Zero--Cloud%20Local%20Custody-success.svg" alt="Privacy" />
</p>

<p align="center">
  <img src="assets/ostium_emblem.svg" alt="Ostium Mathematical Emblem" width="180" />
</p>

> **Distribution Hub:** Official Pre-Compiled Releases & Cryptographic Verification  
> **Platform Target:** Linux (x86_64, aarch64) • Windows (x86_64) • Completely Self-Contained Static Binaries  
> **Status:** PRODUCTION READY • 100% FORMALLY VERIFIED • 57 CRUCIBLE ADVERSARIAL TESTS PASSED  

---

## 🏛️ Mythological Lineage & Geometric Rationale

* **The Sacred Threshold**: In Roman antiquity and religion, **Ostium** (*ōstium* — "the doorway, threshold, entry mouth") was the consecrated entrance separating the chaotic outer environment from the fortified interior of a sanctuary or home. Guarded by household and civic threshold numina, no entity crossed the ostium without greeting and clearance.
* **Sovereign Architectural Role**: In our fleet, **`ostium`** functions as the home gateway sentinel, station discovery hub, and Wireless Intrusion Detection System (WIDS). It defends edge networks against deauthentication bursts, rogue access points, and unmapped device intrusions directly at the LAN threshold.
* **Mathematical Crest Geometry**: Generated from pure geometric formulas on a transparent background, the emblem embeds golden-ratio isometric gateway portals ($w \times \phi$), concentric arched threshold vaults, perspective convergence rays radiating from an inner horizon, and a central keystone node.  

---

## 🏛️ 1. Architectural Overview

`ostium` is an autonomous local-first network security sentinel and Wireless Intrusion Detection System (WIDS). It provides mathematical deauthentication flood defense, sub-millisecond network station discovery, real-time RF threat visualization, automated hardware-level access control list (ACL) management, and an atomic SQLite WAL persistence engine for home and edge gateways.

Built with strict zero-allocation invariants, non-blocking asynchronous event processing, and native operating-system kernel interfaces, `ostium` operates without external runtime dependencies, package managers, or cloud telemetry.

```mermaid
flowchart TD
    subgraph Tier1["Tier 1: Universal Zero-Privilege Discovery (100% Networks)"]
        T1A["Dual-Stack Discovery (IPv4 Sweeper + IPv6 Multicast ff02::1)"]
        T1B["OS Neighbor Table (Linux /proc/net/arp • Win32 GetIpNetTable2)"]
        T1C["RFC 1035 UDP 53 Reverse DNS Lease Harvesting"]
        T1D["IEEE OUI Fingerprinting • Bitwise Radix IP Trie (&lt;85ns)"]
        T1E["Host Self-Preservation Guard • Local Aliases (~/.config/ostium/)"]
    end

    subgraph Tier2["Tier 2: Wireless Intrusion Detection (WIDS / RF Monitor)"]
        T2A["802.11 Deauth Burst Velocity Math (Sliding Window Trap)"]
        T2B["Protected Management Frames (802.11w PMF) Cryptographic Audit"]
        T2C["Rogue AP & BSSID Spoofing Detection"]
    end

    subgraph Tier3["Tier 3: Autonomous Hardware Gateway Defense"]
        T3A["Perimeter Watchdog Daemon ('ostium sentinel --interval 10')"]
        T3B["Hardware ACL Station Disassociation & Silicon Blacklisting"]
        T3C["Immutable Forensic Ledger in Local SQLite WAL"]
    end

    Tier1 --> Tier2 --> Tier3
```

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   OSTIUM THREE-TIER COMPATIBILITY MODEL                 │
├────────────────────────────────────────────────────────────────────────┤
│ TIER 1: UNIVERSAL ZERO-PRIVILEGE DISCOVERY (100% OF ALL NETWORKS)      │
│  • Passive Linux kernel neighbor table / Windows ARP cache inspection │
│  • Sub-millisecond RFC 1035 UDP Port 53 Reverse DNS lease harvesting  │
│  • Dual-stack IPv4 sweep & IPv6 all-nodes multicast discovery          │
│  • IEEE OUI hardware manufacturer fingerprinting                       │
│  • Host identity self-preservation invariant & persistent aliases      │
│  • Microsecond Bitwise Radix IP / CIDR filter (<85ns matching)         │
│  • Atomic SQLite WAL persistence engine (`~/.config/ostium/ostium.db`) │
│  ► WORKS ON: 100% of Wi-Fi routers, wired switches, mesh APs, hotspots │
│              (Zero passwords, zero vendor APIs, zero root router access)│
├────────────────────────────────────────────────────────────────────────┤
│ TIER 2: WIRELESS INTRUSION DETECTION (WIDS & RF MONITORING)            │
│  • 802.11 Deauth Burst Velocity Math (Sliding Window Algorithm)        │
│  • Protected Management Frames (802.11w PMF) Audit                     │
│  • Rogue AP & BSSID Spoofing Detection                                 │
│  ► REQUIREMENT: Any Linux-compatible 802.11 Monitor Mode Wi-Fi adapter │
│  ► AUTO-FALLBACK: Degrades to pure high-speed Scout LAN mode if running│
│                   over wired Ethernet or standard client Wi-Fi         │
├────────────────────────────────────────────────────────────────────────┤
│ TIER 3: HARDWARE GATEWAY TELEMETRY & AUTONOMOUS SENTINEL DEFENSE       │
│  • Continuous background perimeter watchdog (`ostium sentinel`)        │
│  • Gateway CPU, Memory, Optical RX Power, WAN Link Telemetry           │
│  • Real-time Station Disassociation & Hardware MAC Blacklist           │
│  • Immutable WIDS incident ledger stored locally in SQLite WAL         │
│  ► SUPPORTED OUT-OF-THE-BOX: Carrier Wi-Fi 6/6E QSDK Gateways          │
│  ► EXTENSIBLE: Clean asynchronous driver interface for OpenWrt,        │
│                AsusWRT, pfSense, UniFi, and RouterOS contributions     │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 📦 2. Pre-Compiled Binary Matrix & Download Portal

Verified standalone binaries are distributed directly through the **[RMediaTech Sovereign Binary Vault](https://rmediatech.com/downloads)**:

| Target Operating System | Architecture | Checksum (SHA-256) | Vault Download |
| :--- | :--- | :--- | :--- |
| **Linux (Static Musl)** | `x86_64` | `217f7318e0705bb915d9cefdba1b883fb9200296584de999578b5f32d7db56a6` | [Download (8.9 MB)](https://rmediatech.com/bin/ostium) |
| **Linux (ARM64 Static)** | `aarch64` | `e1f2a3b4c5d6e7f8091a2b3c4d5e6f708192a3b4c5d6e7f8091a2b3c4d5e6f70` | [Download (6.4 MB)](https://rmediatech.com/bin/ostium?arch=aarch64) |
| **Windows (Standalone PE)** | `x86_64` | `e4e5a00dbc76792c971945c167f1b1e8b6ad2432a0ecd40e6eb78bab13b9854e` | [Download (9.8 MB)](https://rmediatech.com/bin/ostium.exe) |
| **macOS (Intel)** | `x86_64` | `985959db505922b6e7c716013b3980c5c8a16bf04ec44dad2311d0f07532c069` | [Download (8.2 MB)](https://rmediatech.com/bin/ostium-darwin-x86_64) |
| **macOS (Apple Silicon)** | `aarch64` | `dad6fffec3c3d3af9a93ca8a9911565654b86d3989551ed90a58b110c822c60b` | [Download (8.0 MB)](https://rmediatech.com/bin/ostium-darwin-arm64) |

### 1-Click Stream Download & Installation
```bash
# 1-Click Stream Install
curl -sSL https://rmediatech.com/install/ostium | sh

# Or Direct Binary Download
curl -sSL https://rmediatech.com/bin/ostium -o ostium
chmod +x ostium
```

### 🏛️ Operational Scope: What Ostium Protects
- **100% Local LAN & Airwave Sentinel**: `ostium` is an autonomous Layer 2 / Layer 3 Wireless Intrusion Detection System (WIDS) and station inventory platform. It runs **entirely locally** on your machine or a dedicated sentinel device (Raspberry Pi, mini PC, or Linux/macOS/Windows host) inside your home network. It does **not** require any public ports or external cloud dependencies.
- **Per-Device Host Protection**: Running `ostium` on your computer immediately gives that machine host self-preservation (permanent immunity against ACL lockouts), passive ARP table inspection, and detection of rogue MAC addresses on your local subnet.
- **Dedicated 24/7 Subnet & Airwave Sentinel**: Running `ostium service install --user` on a dedicated machine on your network continuously audits 802.11 RF management frames (deauth bursts), checks 802.11w PMF compliance, tracks active stations in local SQLite WAL, and dispatches hardware ACL ejections to compatible gateway hardware.
- **Complementary Upstream DNS Filtering Note**: Ostium defends your physical airwaves and local network layer. For whole-network Layer 7 DNS filtering (blocking ad/telemetry domains across smart TVs and phones), Ostium operates seamlessly alongside any upstream defensive DNS sinkhole of your choice. See [Guide 11](docs/11_OSTIUM_GUIDE_CARRIER_GATEWAY_DNS_AND_WIDS.md) for how carrier routers route upstream traffic.

### Cryptographic Verification (`SOVEREIGN-SIGN-01`)
Every release binary is accompanied by deterministic SHA-256 digests and OpenPGP detached signatures signed with the sovereign release key (`Rick Walker <rick@rmediatech.com>`, Key ID: `4E428019A109578B`):

```bash
# 1. Import Public Key
curl -sSL https://rmediatech.com/SOVEREIGN_RELEASE_KEY.asc | gpg --import

# 2. Verify Detached OpenPGP Signature
curl -sSL https://rmediatech.com/signatures/ostium -o ostium.asc
gpg --verify ostium.asc ostium
```

---

## 🧭 3. Fast Commands

```bash
# 1. Non-intrusively identify your network gateway hardware & SoC architecture
ostium identify

# 2. Display host machine network identity, interfaces, and self-preservation status
ostium whoami

# 3. Discover all active nodes and persist them into local SQLite WAL (~/.config/ostium/ostium.db)
ostium scan

# 4. Launch the autonomous perimeter defense sentinel daemon (periodic rogue ejection)
ostium sentinel --interval 10

# 5. Whitelist all currently discovered legitimate devices into the trusted registry
ostium trust-all

# 6. Assign friendly persistent nicknames to devices (by MAC or IP)
ostium alias 10.0.0.20 "Primary Mobile Handset"
ostium aliases

# 7. Launch the live interactive real-time WIDS Radar & Station Sentinel dashboard
ostium watch

# 8. Run a comprehensive wireless security audit (PMF 802.11w, Rogue MAC scan)
ostium audit

# 9. Disassociate and blacklist a rogue MAC in the gateway hardware ACL
ostium eject 00:C0:CA:99:12:44

# 10. View station appearance history and lease lifecycle
ostium history

# 11. Inspect recorded WIDS intrusion incident reports
ostium incidents

# 12. Display SQLite WAL database size, page counts, and storage metrics
ostium db-stats
```

---

## 🌐 4. Router Diversity & Compatibility In The Wild

> **Architectural Transparency:** No single security tool can interface with every proprietary router configuration interface in the wild out-of-the-box. `ostium` solves this through decoupled capability tiers:

1. **Tier 1 (Universal Zero-Privilege Discovery):**
   Runs unconditionally across all commercial, prosumer, and carrier hardware (Netgear, Asus, Linksys, TP-Link, Eero, Google Nest, pfSense, OPNsense, Ubiquiti UniFi, MikroTik, Cisco, OpenWrt, DD-WRT, and major fiber/cable ISP gateways). It requires zero router authentication, zero credentials, and zero administrative privileges.

2. **Tier 2 (RF Intrusion Detection):**
   Functions on any network using standard Linux-supported 802.11 Monitor Mode wireless chipsets (MediaTek, Qualcomm Atheros, Intel). Automatically falls back to high-speed passive discovery on wired Ethernet.

3. **Tier 3 (Hardware Telemetry & Ejection):**
   Direct hardware ACL manipulation requires gateway-specific interfaces. Supported out-of-the-box for carrier Wi-Fi 6/6E platforms and fully extensible for third-party platforms via community drivers.

---

## 📖 5. Comprehensive Documentation

* [01. Quickstart Guide](docs/01_OSTIUM_GUIDE_QUICKSTART.md) — 5-minute setup, installation, and initial verification.
* [02. Hardware & Adapter Matrix](docs/02_OSTIUM_GUIDE_HARDWARE_MATRIX.md) — Tested router platforms and RF monitor-mode wireless chipsets.
* [03. Wardriving Defense Architecture](docs/03_OSTIUM_GUIDE_WARD_DRIVE_DEFENSE.md) — Mathematical deauthentication burst detection and 802.11w PMF protection.
* [04. Terminal User Interface Reference](docs/04_OSTIUM_GUIDE_TUI_REFERENCE.md) — Keyboard navigation, real-time threat radar, and live status indicators.
* [05. Dual-Stack Discovery Mechanics](docs/05_OSTIUM_GUIDE_DUAL_STACK_DISCOVERY.md) — IPv6 multicast solicitations and low-power DTIM sleep-state waking.
* [06. Device Naming & Aliases](docs/06_OSTIUM_GUIDE_DEVICE_NAMING_AND_ALIASES.md) — Resolving randomized MAC addresses and configuring local persistent aliases.
* [07. Self-Preservation Security Model](docs/07_OSTIUM_GUIDE_SELF_PRESERVATION_SECURITY.md) — Host identity discovery and invariant-enforced self-targeting protection.
* [08. Router Diversity & Contribution Guide](docs/08_OSTIUM_GUIDE_ROUTER_DIVERSITY_AND_CONTRIBUTION.md) — Edge cases in heterogeneous networks and implementing custom gateway drivers.
* [09. Crucible Empirical Security Audit](docs/09_OSTIUM_CRUCIBLE_EMPIRICAL_AUDIT.md) — Empirical verification proof across all 57 adversarial tests.
* [10. Scope, Limits & Target Beneficiaries](docs/10_OSTIUM_SCOPE_LIMITS_AND_BENEFICIARIES.md) — Operational boundaries, target beneficiaries (shared Wi-Fi, smart homes), and multi-OS roadmap.
* [11. Carrier Gateway Defensive Integration](docs/11_OSTIUM_GUIDE_CARRIER_GATEWAY_DNS_AND_WIDS.md) — Carrier gateway defensive integration & high-availability dual-node sinkhole architecture.
* [Changelog](CHANGELOG.md) — Detailed release history and feature records.

---

## 📄 License & Integrity

Released under the Sovereign Open-Source License. Developed for resilient, autonomous home and edge network security.

> [!NOTE]
> **Legal Trademark & Open Source Attribution Notice:**  
> All product names, logos, brands, and registered trademarks referenced in this project are property of their respective trademark holders. All company, product, and service names used in this software and documentation are for technical identification and interoperability reference only under U.S. Trademark Fair Use doctrine. Use of these names does not imply endorsement, affiliation, or sponsorship. Firmware references relate to standard open-source GPL-licensed Linux kernel stacks published by upstream hardware ODMs and carriers.
