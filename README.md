<div align="center">

# DG AdminPanel

### Advanced Administrative Platform for FiveM

![Version](https://img.shields.io/badge/version-1.2.0-blue.svg)
![License](https://img.shields.io/badge/license-Commercial-red.svg)
![Framework](https://img.shields.io/badge/framework-QBCore%20%7C%20ESX%20%7C%20Standalone-green.svg)

Modern NUI admin system for server operations, moderation, management analytics, and team workflows.

[Overview](#overview) • [Access--Beta](#access--beta) • [Features](#features) • [Installation](#installation) • [Configuration](#configuration) • [Ecosystem](#ecosystem) • [Support](#support)

---

</div>

## Overview

DG AdminPanel is a full administrative suite for FiveM communities. It gives staff one interface for moderation, player support, server controls, management operations, permissions, and live operational visibility.

The platform is built for teams that need consistent staff workflows at scale, not just one-off admin commands. It combines day-to-day moderation tools with management, reporting, and observability so your team can respond quickly while keeping operations organized.

| Property | Value |
|----------|-------|
| Resource Name | dg-adminmenu |
| Manifest Name | dg-adminpanel |
| Version | 1.2.0 |
| Framework Support | QBCore, ESX, Standalone |
| License | Commercial |
| Admin Panel Listing | https://dg-scripts.tebex.io/category/admin-panel |
| Intended Audience | Serious RP and community-driven FiveM servers |

---

## Access & Beta

### Purchase / Access

- Public listing: https://dg-scripts.tebex.io/category/admin-panel
- Resource package: DG AdminPanel (dg-adminmenu)
- License model: commercial resource with active updates

### Beta Testing Program

Want early access to upcoming features and fixes before public release? We are accepting beta testers.

Beta testers receive:
- Access to pre-release builds
- Early testing of new tabs, moderation actions, and management workflows
- Priority feedback review for bug reports and UX improvements

What we expect from beta testers:
- Structured bug reports with reproduction steps
- Environment details (framework, server build, dependencies)
- Fast feedback on usability, permission edge-cases, and performance

How to apply:
1. Contact DreadedGScripts through your normal support channel.
2. Include server size, framework, and typical staff count.
3. Share why your team is a good fit for staged testing.

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
- Staff-focused action grouping for faster response during incidents

---

### Inventory, Vehicle, and Utility Tools

- Item management for self or target player
- Remove items and clear inventories
- Spawn, repair, and remove vehicles
- Player model controls
- World utility controls (time/weather/entity cleanup)
- Utility operations designed for both live incidents and scheduled maintenance

---

### Management Suite

- Job/department management controls
- Employee distribution views
- Business balance operations
- Rank and role administration for job systems
- Broadcast messaging tools for teams and organizations
- Centralized workflows to reduce command fragmentation across staff teams

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
- High-level metrics to help leads triage performance or staffing issues quickly

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
- Scales from small staff teams to multi-tier management structures

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

Recommended startup order:
1. Database and bridge resources
2. Logging/communication resources
3. DG AdminPanel and optional UI enhancements

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
5. Run an internal permission audit before moving to production.

---

## Ecosystem

DG AdminPanel works with the broader DG stack:

- dg-bridge: unified framework integration layer
- dg-discord-bot: Discord logging and workflow integration
- dg-notifications: optional advanced notification UI

---

## Support

For setup support, feature questions, and licensing details, contact DreadedGScripts through your standard support channel.
