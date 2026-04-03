<div align="center">

# 🛡️ DG AdminPanel

### Advanced Admin & Anti-Cheat System for FiveM

![Version](https://img.shields.io/badge/version-1.2.0-blue.svg)
![License](https://img.shields.io/badge/license-Commercial-red.svg)
![Framework](https://img.shields.io/badge/framework-QBCore%20%7C%20ESX%20%7C%20Standalone-green.svg)

**Full-featured NUI admin panel with integrated anti-cheat detection system**

[Features](#-features) • [Installation](#-installation) • [Commands](#-commands) • [Configuration](#%EF%B8%8F-configuration) • [Support](#-support)

---

</div>

## 📋 Overview

**DG AdminPanel** is a comprehensive administrative and anti-cheat solution for FiveM servers, featuring a modern NUI interface, real-time player monitoring, advanced permission systems, and integrated cheat detection with AI-powered suggestions.

| Property | Value |
|----------|-------|
| **Resource Name** | `dg-adminmenu` |
| **Manifest Name** | `dg-adminpanel` |
| **Version** | `1.2.0` |
| **Framework Support** | QBCore, ESX, Standalone |
| **Bridge Dependency** | [`dg-bridge`](https://github.com/DreadedGScripts/dg-bridge) |
| **Discord Dependency** | [`dg-discord-bot`](https://github.com/DreadedGScripts/dg-discord) |
| **Notification Companion** | [`dg-notifications`](https://github.com/DreadedGScripts/dg-notifications) |
| **License** | Commercial (see [`LICENSE.txt`](LICENSE.txt)) |

---

## ✨ Features

### 🎮 Admin Panel Tabs

<table>
<tr>
<td width="50%">

**Core Panels**
- 🏠 **Home** - Dashboard overview
- 👥 **Players** - Player management
- 🏆 **Leaderboard** - Suspect rankings
- 🔧 **Tools** - Admin utilities
- 💼 **Management** - Job/business controls

</td>
<td width="50%">

**Monitoring & Security**
- 🗺️ **Heat Map** - City activity visualization
- 📋 **Reports** - Bug & player reports
- 📊 **Status** - Server metrics
- ⚡ **Triggers** - Detection feed
- 🔐 **Permissions** - Group-based access

</td>
</tr>
</table>

---

| Category | Features |
|----------|----------|
| **Player Actions** | Spectate • Teleport (to/bring) • Freeze/Unfreeze • Revive • Heal • Warn/Kick/Ban |
| **Player Data** | View Reports • Inventory Management • Delete Items • Admin Notes • Clear Lifetime Score |
| **Advanced** | Set Player Model • Live Screen Capture* • Real-time Player Details |

<sup>*Requires `screenshot-basic` resource</sup>

---

### � Multi-Language Support

| Feature | Description |
|---------|-------------|
| **10 Languages** | English, Spanish, French, German, Portuguese, Italian, Dutch, Russian, Chinese, Japanese |
| **Easy Configuration** | Set default language in `config.lua` |
| **Runtime Switching** | Change language without restart |
| **Extensible** | Add new languages easily |
| **Auto-Update UI** | UI automatically updates when language changes |

> 📚 **See [LOCALIZATION.md](LOCALIZATION.md) for detailed documentation**

---

### �🏆 Leaderboard & Monitoring

| Feature | Description |
|---------|-------------|
| **Suspect Ranking** | Real-time detection score leaderboard |
| **Live Updates** | Automatic score refresh and sorting |
| **Quick Actions** | Direct access to high-risk players |

---

### 🔧 Admin Tools

<details>
<summary><b>Player Tools</b></summary>

- 🎁 **Item Management** - Browse framework items, give to self/player, clear inventory
- 🚗 **Vehicle Control** - Spawn custom vehicles, fix, delete nearby
- 👤 **Model Control** - Change player appearance

</details>

<details>
<summary><b>Admin Powers</b></summary>

- 🛡️ **God Mode** - Invincibility toggle
- 👻 **Invisibility** - Hide from players
- 🚀 **Noclip** - Free camera movement
- 🎯 **Teleport** - Instant waypoint teleportation
- 🦴 **X-Ray/Skeleton View** - See through walls

</details>

<details>
<summary><b>World Control</b></summary>

- 🌍 **Entity Management** - Clear nearby objects/vehicles
- ⏰ **Time Control** - Set/freeze world time
- 🌤️ **Weather Control** - Change weather conditions
- 🤖 **NPC Possession** - Control/possess NPCs

</details>

---

### 💼 Server Management

**Job System Integration**
- 📊 Visual charts (employee distribution, salary breakdown)
- 💰 Business account management (balance lookup, deposit/withdraw)
- 📢 Job broadcast messaging with presets & history
- 👔 Set player rank for any job/grade

**Business Tools**
- Real-time job overview cards
- Employee distribution analytics
- Financial transaction controls

---

### 🗺️ Heat Map

Real-time city activity visualization with auto-refresh, manual controls, zoom/pan, and live player count indicators.

---

### 📋 Reports System

| Report Type | Workflow |
|-------------|----------|
| **Player Reports** | Open → In Review → Closed |
| **Bug Reports** | `/reportbug <message>` command |
| **Management** | Assign to admin, delete, notification system |

---

### 📊 Server Status Dashboard

- ⏱️ Server uptime & player counts
- 💻 FPS • CPU • Memory metrics
- 🔗 Discord & database connection status
- 📈 Activity metrics & pending report count

---

### ⚡ Triggers & Detection Feed

**Real-time monitoring with advanced filtering:**

| Filter Type | Options |
|-------------|---------|
| **Category** | Detection • Menu • Security • Admin Actions |
| **Severity** | Critical • Medium • Low |
| **Time Range** | Last Hour • 24H • Session • All |

**Features:** Statistics cards, clear old logs, live push updates

---

### 🔐 Permission System

**Group-Based Access Control**
- ✏️ Create/edit/delete permission groups
- 👥 Assign groups to admins by license
- 🛡️ Protected group restrictions
- 📝 Permission audit log with search/filter
- 💾 Persistent storage: `data/admin_permissions.json`

---

## 🛡️ Anti-Cheat & Security

### 🔍 Detection System

**Multi-Layer Protection**
- ✅ Client-side detection threads
- ✅ Server-side validation & scoring
- ✅ Suspicion scoring with repeated-detection tracking
- 🤖 AI suggestion pipeline (toggleable via `enableAISuggestions`)

### 🎯 Detection Categories

<table>
<tr>
<td width="33%" valign="top">

**Movement**
- Speed anomalies
- Flying/noclip detection
- Super jump detection
- Spawn spam checks

</td>
<td width="33%" valign="top">

**Combat**
- Godmode detection
- Health anomalies
- Armor anomalies
- Rapid fire detection

</td>
<td width="33%" valign="top">

**Exploitation**
- Money changes
- Blacklist enforcement
- Menu/trainer indicators
- Entity spawn abuse

</td>
</tr>
</table>

### 🚫 Anti-Nuke Protection

| Feature | Description |
|---------|-------------|
| **Entity Rate Limiting** | Prevent spawn flooding |
| **Blacklist Cleanup** | Auto-remove prohibited entities |
| **Explosion Control** | Rate-limit projectiles/explosions |
| **Auto-Response** | Optional kick for extreme abuse |

### 🔒 Security Module

Server-side security helpers in `server/security.lua`:

```lua
-- Rate Limiting
exports['dg-adminmenu']:IsRateLimited(source, action, limit, timeWindow)
exports['dg-adminmenu']:IsCriticalActionLimited(source, action)

-- Input Validation
exports['dg-adminmenu']:ValidateString(input, pattern, maxLength)
exports['dg-adminmenu']:ValidateNumber(input, min, max)
exports['dg-adminmenu']:ValidatePlayerId(playerId)
exports['dg-adminmenu']:SanitizeInput(input)

-- Security Logging
exports['dg-adminmenu']:LogSecurityEvent(eventType, source, details)
exports['dg-adminmenu']:GetSecurityLogs(filters)

-- Resource Protection
exports['dg-adminmenu']:VerifyResourceIntegrity()
exports['dg-adminmenu']:SecureRegisterNetEvent(eventName, handler)
```

---

## 💾 Database & Logging

### 📊 Auto-Created Tables

```sql
dg_aicheatdetect_logs       -- Detection event history
dg_aicheatdetect_bans       -- Ban records
dg_aicheatdetect_playerinfo -- Player tracking data
dg_admin_reports            -- Bug & player reports
dg_discord_threads          -- Discord integration cache
```

### 📝 Admin Action Logging

All admin actions are logged as trigger type `admin` and visible in the **Triggers** tab under the `Admin Actions` filter.

---

## 📦 Installation

### Required Dependencies

```lua
ensure oxmysql        -- Database connector
ensure dg-bridge      -- Framework abstraction layer
ensure dg-discord-bot -- Discord integration
ensure dg-adminmenu   -- This resource
```

### Optional Dependencies

```lua
ensure screenshot-basic -- For live screen capture feature
ensure dg-notifications -- For external detection popup alerts
```

### ⚙️ server.cfg Order

```cfg
ensure oxmysql
ensure dg-bridge
ensure dg-discord-bot
ensure dg-adminmenu
ensure dg-notifications # optional
ensure screenshot-basic  # optional
```

> **Note:** Ensure dependencies load in the correct order to prevent initialization errors.

---

## 🎮 Commands

| Command | Key Binding | Description |
|---------|-------------|-------------|
| `/dgadminmenu` | `PAGEDOWN` | Open admin panel |
| `/reportbug <message>` | - | Submit bug report |

---

## ⚙️ Configuration

Main configuration file: **`config.lua`**

### 🔑 Key Settings

```lua
Config.framework = 'qbcore'              -- qbcore | esx | standalone
Config.detectionEnabled = true           -- Enable anti-cheat system
Config.menuDetectionEnabled = true       -- Detect mod menus
Config.enableAISuggestions = false       -- AI-powered suggestions
Config.antiNukeEnabled = true            -- Anti-nuke protection
Config.criticalCheatKickBanEnabled = true -- Auto-action on critical cheats
Config.autoBanCriticalCheats = false     -- Automatic bans
Config.enableCharacterPreview = true     -- Character preview in UI
Config.enableTrollCommands = false       -- Fun admin commands
```

---

## 📤 Exports

### Client Exports

```lua
exports['dg-adminmenu']:getPedStatus()
```

### Server Exports

```lua
-- Player Data
exports['dg-adminmenu']:getPlayerCount()
exports['dg-adminmenu']:getSuspicionScore(source)

-- Security Module (see Security section above for full list)
exports['dg-adminmenu']:IsRateLimited(...)
exports['dg-adminmenu']:ValidateString(...)
-- ... (9 additional security functions)
```

---

## 🔮 Future Updates

### Planned Features

- 🎒 **Inventory Compatibility** - Patches for `ps-inventory` and `ox_inventory` on request
- 🔌 **Conflict Resolution** - Patches for overlapping admin/moderation resources on request
- 🌐 **Multi-Language** - Localization support
- 📱 **Mobile UI** - Responsive design improvements

---

## 📚 Related Resources

| Resource | Description |
|----------|-------------|
| [`dg-bridge`](https://github.com/DreadedGScripts/dg-bridge) | Framework abstraction layer |
| [`dg-discord-bot`](https://github.com/DreadedGScripts/dg-discord) | Discord integration API |
| [`dg-notifications`](https://github.com/DreadedGScripts/dg-notifications) | External popup notifications for detections/score updates |
| [`SERVER_CFG_PERMISSIONS.txt`](SERVER_CFG_PERMISSIONS.txt) | Permission configuration guide |
| [`TERMS.md`](TERMS.md) | Terms of service & support |
| [`RELEASE_CHECKLIST.md`](RELEASE_CHECKLIST.md) | Pre-release validation checklist |

---

## 📞 Support

**Commercial License Holders:**
- Contact DG-Scripts for installation, configuration, and bug support
- See [`TERMS.md`](TERMS.md) for detailed support scope
- Provide order ID with all support requests

**Documentation:**
- [`LICENSE.txt`](LICENSE.txt) - License terms & restrictions
- [`SECURITY.md`](SECURITY.md) - Security best practices
- [`SERVER_CFG_PERMISSIONS.txt`](SERVER_CFG_PERMISSIONS.txt) - Permission setup

---

<div align="center">

**DG AdminPanel** • Advanced FiveM Administration

*Built with ❤️ by DG-Scripts*

</div>

### 🔔 Admin Notification System

`dg-adminmenu` supports two notification paths:

- Built-in admin notification flow inside `dg-adminmenu`
- External popup companion via `dg-notifications` (recommended for themed realtime alert cards)

To enable external popups, ensure `dg-notifications` is started after `dg-adminmenu`.

| Feature | Description |
|---------|-------------|
| **Real-Time Alerts** | Instant notifications to all online admins |
| **Priority Levels** | Critical, High, Medium, Low with visual indicators |
| **Event Types** | Cheat detection, reports, bans/kicks, commands, system alerts |
| **Visual Popups** | Animated notification cards with auto-dismiss |
| **Sound Alerts** | Audio feedback for critical events |
| **History Tracking** | Persistent notification history (max 50 per admin) |
| **Interactive** | Click notifications to view player details |
| **Multi-Language** | Fully localized notification messages |
| **Configurable** | Enable/disable specific notification types |
| **Discord Integration** | Optional webhook for critical alerts |

> 📚 **See [ADMIN_NOTIFICATIONS.md](ADMIN_NOTIFICATIONS.md) for detailed documentation**

---
