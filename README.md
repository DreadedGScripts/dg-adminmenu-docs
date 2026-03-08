<div align="center">

# 🛡️ DG AdminPanel

### Advanced Admin & Anti-Cheat System for FiveM

![Version](https://img.shields.io/badge/version-1.2.0-blue.svg)
![License](https://img.shields.io/badge/license-Commercial-red.svg)
![Framework](https://img.shields.io/badge/framework-QBCore%20%7C%20ESX%20%7C%20Standalone-green.svg)

**Full-featured NUI admin panel with integrated server management tools**

[Features](#-features) • [Installation](#-installation) • [Commands](#-commands) • [Configuration](#%EF%B8%8F-configuration) • [Support](#-support)

---

</div>

## 📋 Overview

**DG AdminPanel** is a comprehensive administrative solution for FiveM servers, featuring a modern NUI interface, real-time player monitoring, advanced permission systems, and integrated security features.

| Property | Value |
|----------|-------|
| **Resource Name** | `dg-adminmenu` |
| **Manifest Name** | `dg-adminpanel` |
| **Version** | `1.2.0` |
| **Framework Support** | QBCore, ESX, Standalone |
| **Bridge Dependency** | [`dg-bridge`](https://github.com/DreadedGScripts/dg-bridge) |
| **Discord Dependency** | [`dg-discord-bot`](https://github.com/DreadedGScripts/dg-discord) |
| **License** | Commercial |

---

## ✨ Features

### 🎮 Admin Panel Tabs

<table>
<tr>
<td width="50%">

**Core Panels**
- 🏠 **Home** - Dashboard overview
- 👥 **Players** - Player management
- 🔧 **Tools** - Admin utilities
- 💼 **Management** - Job/business controls

</td>
<td width="50%">

**Monitoring & Security**
- 🗺️ **Heat Map** - City activity visualization
- 📋 **Reports** - Bug & player reports
- 📊 **Status** - Server metrics
- ⚡ **Activity** - Server event feed
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

### 🏆 Player Monitoring

| Feature | Description |
|---------|-------------|
| **Player Overview** | Real-time player activity tracking |
| **Live Updates** | Automatic player list refresh |
| **Quick Actions** | Direct access to player management tools |

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

### 🔔 Admin Notifications

Real-time alerts are delivered to online admins for key moderation and security events.

| Notification Type | Example |
|-------------------|---------|
| **Cheat Detection** | Godmode, aimbot, rapid-fire flags |
| **Suspicious Activity** | High-risk behavior score alerts |
| **Reports** | New player/bug reports submitted |
| **Admin Actions** | Warn, kick, ban, command activity |
| **System Alerts** | Resource or server warnings |

---

### 📊 Server Status Dashboard

- ⏱️ Server uptime & player counts
- 💻 FPS • CPU • Memory metrics
- 🔗 Discord & database connection status
- 📈 Activity metrics & pending report count

---

### ⚡ Activity Feed

**Real-time server activity monitoring with advanced filtering:**

| Filter Type | Options |
|-------------|---------|
| **Category** | Security • Admin Actions • Player Events |
| **Time Range** | Last Hour • 24H • Session • All |

**Features:** Statistics cards, activity logs, live push updates

---

### 🔐 Permission System

**Group-Based Access Control**
- ✏️ Create/edit/delete permission groups
- 👥 Assign groups to admins by license
- 🛡️ Protected group restrictions
- 📝 Permission audit log with search/filter
- 💾 Persistent storage: `data/admin_permissions.json`

---

## 🛡️ Security Features

### 🔒 Server Protection

**Multi-Layer Security**
- ✅ Server-side validation
- ✅ Rate limiting and abuse prevention
- ✅ Comprehensive logging system
- ✅ Automated security responses

### 🔒 Security Module

Server-side security helpers provide rate limiting, input validation, event logging, and resource protection features.

---

## 💾 Database & Logging

### 📊 Auto-Created Tables

The system automatically creates database tables for:
- Ban records and player tracking
- Bug and player reports
- Discord integration
- Admin action logging

### 📝 Admin Action Logging

All admin actions are logged and visible in the activity feed with timestamp, actor, and target information.

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
```

### ⚙️ server.cfg Order

```cfg
ensure oxmysql
ensure dg-bridge
ensure dg-discord-bot
ensure dg-adminmenu
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
Config.enableCharacterPreview = true     -- Character preview in UI
Config.enableTrollCommands = false       -- Fun admin commands
Config.logBansToDiscord = true           -- Discord ban notifications
```

Additional security and detection settings are available in the configuration file.

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

-- Security Module
exports['dg-adminmenu']:IsRateLimited(...)
exports['dg-adminmenu']:ValidateString(...)
-- Additional security and validation functions available
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

---

## 📞 Support

**Commercial License Holders:**
- Contact DG-Scripts for installation, configuration, and support
- Provide order ID with all support requests

**Documentation:**
- Configuration details are in your resource `config.lua`
- Permission setup is managed in the in-game Permissions tab
- Security best practices are described directly in this README

---

<div align="center">

**DG AdminPanel** • Advanced FiveM Administration

*Built with ❤️ by DG-Scripts*

</div>
