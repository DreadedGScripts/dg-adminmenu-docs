<div align="center">

# DG AdminPanel

### Advanced Administrative Platform for FiveM

![Version](https://img.shields.io/badge/version-1.2.0-blue.svg)
![License](https://img.shields.io/badge/license-Commercial-red.svg)
![Framework](https://img.shields.io/badge/framework-QBCore%20%7C%20ESX%20%7C%20Standalone-green.svg)

Modern NUI admin system for server operations, moderation, management analytics, and team workflows.

[Overview](#overview) • [Features](#features) • [Installation](#installation) • [Configuration](#configuration) • [Ecosystem](#ecosystem)

---

</div>

## Overview

DG AdminPanel is a full administrative suite for FiveM communities. It gives staff one interface for moderation, player support, server controls, management operations, permissions, and live operational visibility.

| Property | Value |
|----------|-------|
| Resource Name | dg-adminmenu |
| Manifest Name | dg-adminpanel |
| Version | 1.2.0 |
| Framework Support | QBCore, ESX, Standalone |
| License | Commercial |

---

## Features

### Admin Panel Tabs

| Tab | Purpose |
|-----|---------|
| Home | Snapshot dashboard and quick actions |
| Players | Search, inspect, and manage online players |
| Leaderboard | Priority monitoring and fast moderation workflow |
| Tools | Utility actions for admin operations |
| Management | Job and business administration |
| Heat Map | Live activity map with zoom/pan controls |
| Reports | Player and bug report queue management |
| Status | Real-time server health and metrics |
| Triggers | Event timeline and filtering workspace |
| Permissions | Group and access policy management |

---

### Moderation & Player Operations

- Spectate players
- Teleport to player / bring player
- Freeze and unfreeze player
- Revive and heal actions
- Warn, kick, and ban workflow
- View player context and session details
- Notes and moderation history workflow

---

### Inventory, Vehicle, and Utility Tools

- Item management for self or target player
- Remove items and clear inventories
- Spawn, repair, and remove vehicles
- Player model controls
- World utility controls (time/weather/entity cleanup)

---

### Management Suite

- Job/department management controls
- Employee distribution views
- Business balance operations
- Rank and role administration for job systems
- Broadcast messaging tools for teams and organizations

---

### Reports System

| Report Type | Description |
|-------------|-------------|
| Player Reports | Staff review workflow with status tracking |
| Bug Reports | Structured issue intake from users |
| Assignment Flow | Move reports through review and closure |

---

### Status Dashboard

- Server uptime and player counts
- FPS, CPU, and memory summaries
- External service status visibility
- Pending workload indicators for staff

---

### Heat Map

- Real-time map visualization
- Manual and live refresh
- Zoom, pan, and location monitoring
- Live player distribution visibility

---

### Permissions & Access Control

- Group-based permission architecture
- Create, edit, and remove admin groups
- Assign access profiles by staff identity
- Protected group controls
- Audit-friendly permission administration

---

### Localization

Multi-language support for global communities.

Supported languages include:
- English
- Spanish
- French
- German
- Portuguese
- Italian
- Dutch
- Russian
- Chinese
- Japanese

---

## Installation

### Required Dependencies

```cfg
ensure oxmysql
ensure dg-bridge
ensure dg-discord-bot
ensure dg-adminmenu
```

### Optional Dependencies

```cfg
ensure screenshot-basic
ensure dg-notifications
```

---

## Configuration

Primary configuration files:

- config.lua
- data/admin_permissions.json
- locales/*

Recommended setup flow:
1. Configure framework and server options in config.lua.
2. Define staff groups and permission scopes.
3. Select default locale and localization options.
4. Validate tab visibility and action permissions for each staff role.

---

## Ecosystem

DG AdminPanel works with the broader DG stack:

- dg-bridge: unified framework integration layer
- dg-discord-bot: Discord logging and workflow integration
- dg-notifications: optional advanced notification UI

---

## Support

For setup support, feature questions, and licensing details, contact DreadedGScripts through your standard support channel.
