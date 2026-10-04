<p align="center">
  <a href="https://kurbis.host" target="_blank" rel="noopener noreferrer">
    <img src="https://raw.githubusercontent.com/kurbis-host/.github/main/assets/banner.png" alt="kurbis.host banner" width="850" />
  </a>
</p>

<p align="center">
  <a href="https://kurbis.host" target="_blank" rel="noopener noreferrer">
    <img src="https://raw.githubusercontent.com/kurbis-host/.github/main/assets/kurbis.svg" alt="kurbis.host logo" width="96" height="96" />
  </a>
</p>

<h1 align="center">kurbis.host</h1>

<p align="center">
  <strong>Your world waits. Your server doesn’t.</strong><br>
  <em>Effortless, wake-on-connect Minecraft hosting for friend groups.</em><br>
  Sleeps when empty, wakes when you join, snapshots safely in between.
</p>

<p align="center">
  <a href="https://kurbis.host"><img src="https://img.shields.io/badge/Launch%20World-kurbis.host-D5612D?style=for-the-badge&logo=rocket&logoColor=white" alt="Launch on kurbis.host"></a>
  <a href="https://img.shields.io/badge/Minecraft-Java%20%2B%20Bedrock-547237?style=for-the-badge&logo=minecraft&logoColor=white"><img src="https://img.shields.io/badge/Minecraft-Java%20%2B%20Bedrock-547237?style=for-the-badge&logo=minecraft&logoColor=white" alt="Java + Bedrock Crossplay"></a>
  <a href="https://github.com/kurbis-host/Pumpkin"><img src="https://img.shields.io/badge/Engine-Pumpkin%20(Rust)-b45126?style=for-the-badge&logo=rust&logoColor=white" alt="Pumpkin Rust Engine"></a>
  <a href="#specifications-and-free-tier"><img src="https://img.shields.io/badge/Tier-100%25%20Free-302B25?style=for-the-badge" alt="100% Free"></a>
  <a href="#how-it-works"><img src="https://img.shields.io/badge/Sleep%20Timer-5%20Min%20Idle-56584F?style=for-the-badge" alt="5 Min Idle Sleep"></a>
  <a href="#durable-cloud-snapshots-and-1-click-rollback"><img src="https://img.shields.io/badge/Snapshots-Durable%20S3-5E9BB2?style=for-the-badge" alt="Durable S3 Snapshots"></a>
</p>

<p align="center">
  <a href="https://kurbis.host"><strong>Website & Panel</strong></a> •
  <a href="#why-kurbis"><strong>Why Kurbis?</strong></a> •
  <a href="#how-it-works"><strong>How It Works</strong></a> •
  <a href="#key-features"><strong>Features</strong></a> •
  <a href="#the-kurbis-web-panel"><strong>Web Panel</strong></a> •
  <a href="#specifications-and-free-tier"><strong>Specs & Limits</strong></a> •
  <a href="#quick-start"><strong>Quick Start</strong></a> •
  <a href="#frequently-asked-questions"><strong>FAQ</strong></a>
</p>

---

## 🎃 Why Kurbis?

### The hosting ritual is broken.

Playing Minecraft with friends usually comes with an annoying compromise:

- **Pay $10–$25 every month** for a 24/7 rented VPS that sits completely empty 90% of the week.
- **Self-host on your gaming PC**, which means port forwarding, dynamic DNS headaches, leaving your computer running all night, and being the only person who can turn the server on.
- **Use traditional "free" hosts**, only to suffer through 45-minute queue times, laggy hardware, hourly renewal CAPTCHAs, and servers that get deleted if you go on vacation for a week.

### Kurbis is built around your world, not a 24/7 billing meter.

**Kurbis keeps your world ready without keeping a machine burning electricity.**

When anyone in your group wants to play, they simply connect to your server address in Minecraft. The Kurbis gateway catches the connection, wakes your world up in seconds, and connects them seamlessly. When everyone logs off, a 5-minute countdown begins. Once it finishes, Kurbis captures a verified snapshot of your world, stores it safely in durable cloud storage, and releases the infrastructure.

Next day, next week, or next month—connect again, and your world picks up right where you left off.

- ⚡ **Zero server babysitting** — No need to open a dashboard to click "Start" before playing.
- 🎮 **One address, two editions** — Java and Bedrock friends play together in the exact same world.
- 🛡️ **Durable snapshot protection** — Your world data is saved safely to cloud object storage.
- 💸 **100% Free** — 2 GiB RAM, 5 GiB storage, no credit card required, no ads, no countdown renewals.

---

## 🔄 How It Works

Kurbis reimagines the server lifecycle as a clean, automated cycle:

```
┌──────────────────────────────────────────────────────────────────────────┐
│                         THE KURBIS SERVER CYCLE                          │
└──────────────────────────────────────────────────────────────────────────┘

    1. 💤 SLEEP                          2. ⚡ WAKE ON CONNECT
    ────────────────────────             ────────────────────────
    • World rests in cloud storage       • Any player joins in Minecraft
    • 0 CPU, 0 RAM consumed              • Gateway catches connection
    • Domain & IP stay reserved          • Server starts & restores world
               │                                    ▲
               ▼                                    │
    ┌────────────────────────┐           ┌────────────────────────┐
    │     Durable Cloud      │           │     Kurbis Gateway     │
    │     World Snapshot     │           │    (Java + Bedrock)    │
    └────────────────────────┘           └────────────────────────┘
               ▲                                    │
               │                                    ▼
    4. 💾 SNAPSHOT & SLEEP               3. ⛏️ PLAY TOGETHER
    ────────────────────────             ────────────────────────
    • Last player disconnects            • Friends build, mine & explore
    • 5-minute idle countdown runs       • High tick rate, 2 GiB RAM
    • Safe world snapshot captured       • Live logs, web console & OP
```

### The 4 Stages in Detail

1. **Sleep**: When no one is playing, no server process runs. Your world lives securely as an immutable, compressed snapshot in cloud storage.
2. **Wake on Connect**: A player opens Minecraft and connects to `your-world.kurbis.host`. The Kurbis intelligent gateway catches the connection, provisions an isolated worker, restores your world from its snapshot, and seamlessly transitions the player into the game.
3. **Play**: Friends join, explore, build, and adventure together. Low latency, rock-solid tick rates, and full crossplay.
4. **Snapshot**: When the last person logs off, a 5-minute inactivity timer begins. Once it expires, Kurbis cleanly saves the world state, verifies the snapshot in cloud storage, and releases worker capacity.

---

## ✨ Key Features

### 🌐 One Address, True Crossplay (Java + Bedrock)
Stop asking your friends *"Are you on PC or console?"*
- **Single Hostname**: Share one clean address (e.g. `your-world.kurbis.host`).
- **Seamless Crossplay**: Java Edition players (PC, Mac, Linux) and Bedrock Edition players (Windows, iOS, Android, Xbox, PlayStation, Nintendo Switch) play together in the exact same world.
- **Zero Config**: No messy Geyser setups, no separate port forwards, no plugin conflicts.

### ⚡ Powered by Pumpkin (Rust-Native Minecraft Engine)
Kurbis is powered by **[Pumpkin](https://github.com/kurbis-host/Pumpkin)**, a cutting-edge Minecraft server written from the ground up in Rust:
- **Instant Boot**: Boots in a fraction of the time required by traditional bloated Java servers.
- **Memory Efficient**: High-performance multithreading and memory safety without garbage-collection pauses.
- **Buttery-Smooth Ticks**: Reliable 20 TPS performance designed for multiplayer exploration.

### 🛡️ Durable Cloud Snapshots and 1-Click Rollback
Your builds and adventures are too important to lose to server corruption:
- **Automatic Session Saves**: An immutable snapshot is captured every time your server goes to sleep.
- **Manual Backups**: Trigger a manual backup snapshot anytime from the web panel while playing.
- **1-Click Restore**: Creeper blew up your storage room? Accidental lava fire? Roll back to any snapshot in your history instantly.
- **Persistent Worlds**: Your world never expires or gets wiped due to inactivity.

### 🔑 In-Game Control: The `/kurbis` Chat Command
Manage your server without ever leaving the game:
- Are you an operator in-game? Type `/kurbis` in chat.
- Kurbis generates a private, secure, 15-minute one-time link right in your Minecraft chat.
- Click the link to open your server's web management panel—no passwords or logins required!

---

## 🎛️ The Kurbis Web Panel

A management dashboard designed for players, not system administrators:

<p align="center">
  <img src="https://raw.githubusercontent.com/kurbis-host/.github/main/assets/panel-preview.png" alt="Kurbis Management Panel Preview" width="850" />
</p>

- **Live Lifecycle State**: Real-time visibility into whether your world is Sleeping, Waking, Restoring, Online, or Snapshotting.
- **Online Console**: Send operator commands (`/gamemode`, `/time set`, `/give`) directly from your browser while online.
- **Live ANSI Logs**: Real-time server logs with Minecraft and ANSI color rendering.
- **Player & Whitelist Management**: Manage your player roster, whitelist status, and operator permissions with a single click.
- **World Presets & Settings**: Choose between Survival or Creative presets, tweak difficulty, toggle PvP, and configure view distance.
- **Accessible & Responsive**: Fully responsive from 390px mobile screens to large desktop monitors, keyboard navigable, and WCAG AA compliant.

---

## 📊 Specifications and Free Tier

We believe hosting limits should be plainly stated with no hidden asterisks:

| Specification | Kurbis Free Tier | Details |
| :--- | :--- | :--- |
| **Dedicated Memory** | **2 GiB RAM** | Dedicated worker memory per world |
| **World Storage** | **5 GiB** | Persistent S3-compatible cloud snapshot storage |
| **Idle Sleep Timer** | **5 Minutes** | Automatically saves and sleeps after the last player leaves |
| **Editions** | **Java + Bedrock** | Both editions supported out of the box |
| **Server Address** | **Custom Subdomain** | Included free (e.g. `your-world.kurbis.host`) |
| **Player Limit** | **Uncapped** | No artificial player slots; invite your whole group |
| **Snapshots** | **Unlimited Saves** | Automatic session saves + manual backup snapshots |
| **Console & Logs** | **Live SSE Stream** | Real-time web console and color-formatted logs |
| **Price** | **100% Free** | No credit card required. No ads. No deletion timers. |

---

## 🚀 Quick Start

Getting a server up and running takes less than a minute:

1. **Sign In**: Go to **[kurbis.host](https://kurbis.host)** and sign in with your Google or Discord account.
2. **Create Your World**: Pick a name for your world (e.g. `cozy-craft`) and select your game preset (Survival or Creative).
3. **Share the Address**: Copy your server address (`cozy-craft.kurbis.host`) and share it with your friends.
4. **Join & Play**: Open Minecraft (Java or Bedrock) and connect to your address. Kurbis automatically wakes up, restores the world, and lets you in!

---

## ❓ Frequently Asked Questions

<details>
<summary><strong>Does sleeping delete my world, chests, or inventory?</strong></summary>
<br>
<strong>No, never.</strong> When a server sleeps, Kurbis performs a clean save and uploads a full snapshot of your world directory to durable cloud storage. Your buildings, chests, entities, player inventories, and advancements are fully preserved. When the next player connects, that exact snapshot is restored.
</details>

<details>
<summary><strong>Do I or my friends have to open a website before playing?</strong></summary>
<br>
<strong>No!</strong> That’s the magic of wake-on-connect. Anyone who has your server address can simply add it to their Minecraft server list and click "Join". The Kurbis gateway catches the incoming handshake, wakes up your server, and connects the player automatically.
</details>

<details>
<summary><strong>Can my friends wake up the server when I'm not online?</strong></summary>
<br>
<strong>Yes.</strong> You don't need to be at your computer or awake to start the server for your friends. As long as they have the address (and are on your whitelist, if you have one enabled), connecting to the server will trigger the wake cycle.
</details>

<details>
<summary><strong>Can Java and Bedrock players play in the same world together?</strong></summary>
<br>
<strong>Yes.</strong> Kurbis has built-in cross-edition networking. A player on a Windows PC running Java Edition and a player on an iPad or console running Bedrock Edition connect to the exact same hostname and see each other in the game.
</details>

<details>
<summary><strong>What happens if someone stays AFK?</strong></summary>
<br>
The 5-minute inactivity countdown only begins when the online player count drops to zero. As long as at least one player is actively connected to the server, it will stay online.
</details>

<details>
<summary><strong>Can I create manual backups or roll back my world?</strong></summary>
<br>
<strong>Yes.</strong> From the Kurbis web panel at [kurbis.host/app](https://kurbis.host/app), you can trigger manual backups while your server is online, inspect your snapshot history, and restore any previous snapshot with a single click.
</details>

<details>
<summary><strong>Can I upload custom mods or Forge/Fabric modpacks right now?</strong></summary>
<br>
Not in v1. To guarantee sub-second boot times, rock-solid stability, and flawless crossplay, Kurbis currently focuses on curated, high-performance vanilla gameplay powered by Pumpkin. Mod and plugin support is on our roadmap as the Pumpkin ecosystem expands.
</details>

<details>
<summary><strong>How can Kurbis offer this for free without ads?</strong></summary>
<br>
Traditional hosts pay massive data center bills because their servers run 24 hours a day, 7 days a week—even when 95% of those hours are spent hosting an empty world. By putting inactive servers to sleep and restoring them on demand, Kurbis cuts idle compute waste by over 90%, making high-performance free hosting sustainable.
</details>

---

## 🛠️ Technology Stack

Kurbis is engineered with modern, memory-safe, high-performance systems:

- **Control Plane**: Written in **Rust** using Axum, PostgreSQL, and Server-Sent Events (SSE).
- **Smart Gateway**: Custom **Rust** network proxy handling Java hostname routing, Bedrock transport, and waiting-session orchestration.
- **Server Engine**: **[Pumpkin](https://github.com/kurbis-host/Pumpkin)** — the fast, multithreaded Minecraft server built from scratch in Rust.
- **Worker Infrastructure**: Lightweight, isolated container workers with local NVMe caching and S3-compatible snapshot pipelines.
- **Web Interface**: Modern **Next.js** (App Router), Tailwind CSS, accessible UI primitives, and real-time SSE event subscriptions.

---

## 🌐 Community and Links

- 🌍 **Website & Panel**: [kurbis.host](https://kurbis.host)
- 💻 **Control Panel**: [kurbis.host/app](https://kurbis.host/app)
- 🎃 **Pumpkin Minecraft Engine**: [github.com/kurbis-host/Pumpkin](https://github.com/kurbis-host/Pumpkin)
- 🏢 **GitHub Organization**: [github.com/kurbis-host](https://github.com/kurbis-host)

---

<p align="center">
  <sub>Kurbis v1 · Pumpkin-powered Minecraft hosting · <a href="https://kurbis.host">Start your world at kurbis.host</a></sub>
</p>
