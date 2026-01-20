# DutchFinals

A competitive SMP finale game plugin featuring scheduled gameplay, multiple game modes including solo, team battles, and team selection systems. Includes rank-based kits, custom layouts, armor trims, world border mechanics, XP progression, and comprehensive statistics tracking.

## 🎮 Game Modes

### 1. **Normale Finale** (Solo)
Solo last-man-standing battle where everyone fights for themselves.

### 2. **Team Finale** (Blue vs Red)
Classic team battle - Blue team vs Red team.

### 3. **Lifesteal** (Solo & Teams)
- Solo: Fight with lifesteal mechanics
- Teams: Team-based lifesteal battles

### 4. **Teams (2-5 Players)**
Dynamic team selection where players choose from 45 available teams (Team 1 - Team 45):
- Team 2: 2 players per team
- Team 3: 3 players per team
- Team 4: 4 players per team
- Team 5: 5 players per team
- **Features:**
  - Interactive team selection GUI with book
  - Teammates glow green, enemies glow red
  - Friendly fire protection
  - Team-based win conditions
  - Team name tags display
  - Team elimination tracking

## ✨ Core Features

### Gameplay
- ⏰ **Scheduled Gameplay** - Configurable days and times
- 🗺️ **Multiple World Support** - Vote for your favorite maps
- 🎯 **Game Modes** - Solo, Teams (2v2, 3v3, etc.), Lifesteal, Team Selection
- 🌍 **Dynamic World Border** - Shrinks over time to force encounters
- 🎆 **Victory Effects** - Firework displays and custom titles
- 👁️ **Spectator Mode** - Watch the action after elimination
- 🔄 **Automatic World Reset** - FAWE integration for perfect restoration

### Customization
- 🎒 **LuckPerms Rank-Based Kits** - Different kits for different ranks
- ✨ **Player Kit Layouts** - Rearrange inventory to your preference
- 🛡️ **Armor Trims System** - Unlock and customize armor cosmetics
- 📊 **XP & Rank Progression** - Level up through 50+ ranks
- 🎨 **Personal Hologram Stats** - Display your stats above your head

### Statistics & Progression
- 📈 **Comprehensive Stats Tracking** - Wins, losses, K/D, win rate
- 🏆 **Leaderboards** - Top players by wins, kills, level
- 🎖️ **50+ Ranks** - From Recruit to Legend with custom XP requirements
- 💎 **XP Bar Display** - Real-time progression tracking
- 📊 **Personal Stats Command** - View detailed statistics

### Protection & Quality of Life
- 🛡️ **Team Damage Prevention** - Can't hurt teammates
- 🔒 **Hub Protection** - Safe lobby area
- 🚫 **Anti-Exploit** - Crafting blocks, advancement blocks, freeze protection
- 🪧 **Join Signs** - Click signs to join games
- 🔊 **ItemsAdder Sound Integration** - Custom sounds and titles

## 📋 Commands

### Player Commands
| Command | Description |
|---------|-------------|
| `/dutchfinals join` | Join the game |
| `/dutchfinals leave` | Leave the lobby or game |
| `/dutchfinals stats [player]` | View player statistics |
| `/dutchfinals layout` | Customize your kit inventory layouts |
| `/trims` | Open armor trims customization GUI |
| `/checkrank [player]` | Check your or another player's rank and XP |
| `/spectate` | Enter spectator mode (during games) |
| `/leaderboard` | View top players leaderboard |

### Admin Commands
| Command | Description |
|---------|-------------|
| `/dutchfinals help` | Show all commands |
| `/dutchfinals setminplayers <amount>` | Set minimum players required |
| `/dutchfinals setmaxplayers <amount>` | Set maximum players allowed |
| `/dutchfinals setkit <mode> <team> [name]` | Set kit from inventory |
| `/dutchfinals addworld <world>` | Add a world for games |
| `/dutchfinals removeworld <world>` | Remove a world |
| `/dutchfinals enable <world>` | Enable a world |
| `/dutchfinals disable <world>` | Disable a world |
| `/dutchfinals startborder <size>` | Set starting border size |
| `/dutchfinals endborder <size>` | Set ending border size |
| `/dutchfinals speedborder <seconds>` | Set border shrink duration |
| `/dutchfinals stop` | Force stop the current game |
| `/dutchfinals reload` | Reload configuration |
| `/forcestart` | Force start the game countdown |
| `/joinsign create` | Create a join sign |
| `/joinsign remove` | Remove a join sign |
| `/leaderboard create <type>` | Create a leaderboard hologram |

### Kit Setup Commands
Set kits from your current inventory:
- `/dutchfinals setkit normal solo player <rankName>` - Normal solo kit
- `/dutchfinals setkit normal team blue <kitName>` - Blue team kit
- `/dutchfinals setkit normal team red <kitName>` - Red team kit
- `/dutchfinals setkit lifesteal solo player <rankName>` - Lifesteal solo kit
- `/dutchfinals setkit lifesteal team blue <kitName>` - Lifesteal blue team kit
- `/dutchfinals setkit lifesteal team red <kitName>` - Lifesteal red team kit

## 🔑 Permissions

### Player Permissions
- `dutchfinals.join` - Join games (default: true)
- `dutchfinals.leave` - Leave games (default: true)
- `dutchfinals.stats` - View statistics (default: true)
- `dutchfinals.layout` - Edit kit layouts (default: true)
- `dutchfinals.trims` - Use armor trims (default: true)
- `dutchfinals.checkrank` - Check ranks (default: true)
- `dutchfinals.spectate` - Spectate games (default: true)
- `dutchfinals.vote.normal` - Vote for normal mode (default: true)
- `dutchfinals.vote.teamfight` - Vote for team mode (default: true)
- `dutchfinals.vote.lifesteal` - Vote for lifesteal mode (default: true)
- `dutchfinals.vote.map.*` - Vote for maps (default: op)

### Admin Permissions
- `dutchfinals.admin` - Access to all admin commands
- `dutchfinals.forcestart` - Force start games
- `dutchfinals.joinsign` - Create/manage join signs
- `dutchfinals.leaderboard` - Create/manage leaderboards

## ⚙️ Configuration

### Schedule Setup
Configure when games can be played in `config.yml`:
```yaml
schedule:
  enabled: true
  days:
    - SATURDAY
  join-time: "19:30:00"
  start-time: "20:00:00"
```

### Kit System
1. Equip the items you want in the kit
2. Run the appropriate setkit command
3. Players can customize layouts with `/dutchfinals layout`

**Player Layout Customization:**
- Rearrange kit items to preferred inventory slots
- Per-kit layouts (different arrangements for different kits)
- Safe & exploit-proof (no item duplication)
- Persistent across server restarts

### Armor Trims System
Players can unlock and customize armor trims:
- **Materials**: 11 different trim materials to unlock
- **Patterns**: 17 different trim patterns to unlock
- **Unlock System**: Earn trims through gameplay
- **Preview System**: See trims before applying
- **Persistent**: Trims save across sessions

### XP & Rank Progression
- **50+ Ranks**: From Recruit to Legend
- **XP Sources**: Wins (+50 XP), Kills (+10 XP), Participation (+5 XP)
- **XP Bar**: Real-time display in hotbar
- **Rank Prefixes**: Display in chat and holograms
- **Configurable**: Custom ranks and XP in `levels.yml`

### World Setup
1. Create/prepare your game world
2. Run `/dutchfinals addworld <worldname>`
3. Configure border settings with admin commands

### ItemsAdder Integration
Configure custom sounds and titles in `config.yml`:
```yaml
countdown:
  sound-at-start: "dutchfinals:game_start"
  sound-at-10sec: "dutchfinals:countdown_10"

death:
  sound: "dutchfinals:player_death"
  title-type: "itemsadder"
  itemsadder-title: "dutchfinals:death_screen"
```

## 📦 Dependencies

### Required
- **LuckPerms** - Permission system for rank-based kits
- **ItemsAdder** - Custom sounds and titles

### Highly Recommended
- **FastAsyncWorldEdit (FAWE)** - Perfect world restoration (100% accurate)
  - Download: https://www.spigotmc.org/resources/fastasyncworldedit.13932/
  - Restores ALL blocks including cobwebs, water, explosions
  - Fast and efficient snapshot system

### Optional
- **FancyHolograms** - Leaderboard and stats display

### Server Requirements
- **Platform**: Paper/Spigot 1.21.4+
- **Java**: 21+

## 🔄 World Reset System

### ✅ FastAsyncWorldEdit (FAWE) - Recommended
- **100% accurate** world restoration
- Restores ALL blocks including:
  - Cobwebs
  - Water in non-full blocks (stairs, slabs, leaves)
  - Explosion damage
  - All block states
- Fast and efficient snapshot system
- Automatic detection and usage

### ⚠️ Fallback: Manual Block Tracking
- ~85-90% accurate
- May miss cobwebs and water in certain blocks
- Used automatically if FAWE is not installed
- Still functional for basic restoration

## 💾 Database

Supports both SQLite and MySQL for player statistics:
- **SQLite**: Default, no configuration needed
- **MySQL**: Configure in `config.yml` for better performance

Stored data:
- Player statistics (wins, losses, kills, deaths)
- XP and rank progression
- Armor trim unlocks
- Kit layouts
- Personal settings

## 🚀 Installation

1. **Install Dependencies**:
   - LuckPerms
   - ItemsAdder
   - FastAsyncWorldEdit (highly recommended)
   - FancyHolograms (optional)

2. **Install Plugin**:
   - Place `DutchFinals.jar` in your `plugins` folder
   - Restart server

3. **Configure**:
   - Edit `config.yml` for schedule and settings
   - Configure `worlds.yml` for game worlds
   - Set up kits using `/dutchfinals setkit` commands
   - Customize `levels.yml` for XP progression

4. **Setup Worlds**:
   - Add game worlds with `/dutchfinals addworld <world>`
   - Configure border sizes
   - Enable/disable worlds as needed

5. **Create Join Signs** (optional):
   - Use `/joinsign create` while looking at a sign

6. **Create Leaderboards** (optional):
   - Use `/leaderboard create <type>` for hologram leaderboards

7. **Ready to Play!**
   - Players can join with `/dutchfinals join`
   - Customize kits with `/dutchfinals layout`
   - Unlock trims with `/trims`

## 🎯 Gameplay Flow

1. **Schedule Time** - Players join during configured times
2. **Team Selection** - For team modes, players select teams via GUI
3. **World Voting** - Players vote for their preferred map
4. **Mode Voting** - Players vote for game mode (Normal/Team/Lifesteal)
5. **Countdown** - 30-second countdown before start
6. **Game Start** - Players teleport to world with selected kits
7. **Border Shrinks** - World border shrinks over time
8. **Last Standing Wins** - Solo or team victory
9. **Rewards** - XP, stats updates, and progression
10. **World Reset** - Automatic restoration for next game

## 📊 Statistics Tracked

- **Games Played** - Total matches participated
- **Wins** - Total victories
- **Losses** - Total defeats
- **Kills** - Total eliminations
- **Deaths** - Total deaths
- **K/D Ratio** - Kill/Death ratio
- **Win Rate** - Win percentage
- **XP** - Experience points for progression
- **Rank** - Current rank based on XP
- **Mode-Specific Wins** - Normal, Team, Lifesteal wins

## 🏆 Leaderboard Types

- **Total Wins** - Players with most overall wins
- **Normal Wins** - Players with most solo wins
- **Team Wins** - Players with most team wins
- **Lifesteal Wins** - Players with most lifesteal wins
- **Kills** - Players with most eliminations
- **Level** - Players with highest rank/XP

## 👨‍💻 Created By

**Dutchwilco** - [dutchcoding.nl](https://dutchcoding.nl)

## 📞 Support

For issues or questions, contact Dutchwilco.

---

**Version**: 1.0.0  
**Last Updated**: January 2026
