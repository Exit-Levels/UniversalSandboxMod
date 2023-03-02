# Documentation for mod_manifest.json
## General

* Compatibile with version 0.0.1
* Created on *01.03.2023*
* Last Updated: *01.03.2023*
* File should be named mod_manifest.json
* Documentation available at https://exitlevels.github.io/mod_template/mod_manifest_docs.md

## Main
### ModID
This information gives game information about approved mod.
You can submit your modification to us and after *some time* you will get your modID or rejection

If **"mod-id"** is invalid game won't load this mod.

When you are developing mod, set **"mod-id"** to **"dev-mode"**.
Using this, players will get information that this is not approved but in development mod.

Example Usage:

    ...
    "mod-id":"dev-mode"
    ...

    or

    ...
    "mod-id":"ID from our dev tools"
    ...
---
### Author

This is author name.
Example Usage:

    ...
    "author":"Empezeeet"
    ...

---
### Title

Title. This data is shown on:
   
   1. Mod Loading Screen
   2. Mod Tile
   3. Player activity 
   4. Discord RPC
   5. Everywhere your mod is used and/or mentioned

Example Usage:

    ...
    "title":"Very good mod title"
    ...

---
### Desc

Longer description of your mod. **Max 1024 Characters**

Displayed on ModPage and ModInfo

Example Usage:

    ...
    "desc":"This mod is about showing other people how to make mod_manifest.json"
    ...
---
### Short-desc
Shorter Description of your mod. **Max 64 Characters**
Displayed on Mod Tile, DiscordRPC, PlayerActivity.
Example Usage:

    ...
    "short-desc":"mod_manifest.json Template for new ModDevs"
    ...
---

## Game-Settings
Everything about game settings.

### Max-Players
Information about how much player-slots are available.

**Max -> 8**

**Min -> 1**

Example Usage:
    
    ...
    "game-settings": {
        "max-players":4, 
        ...
    }
    ...

---
### Min-players
Minimal players to play mod.

**Min -> 1**
**Max -> 4**

Example Usage:
    
    ...
    "game-settings": {
        "min-players":1, 
        ...
    }
    ...

---
### Max-player-health
Max player health that player can regen to.
If set to 0 players are invincible.

**Max -> 1024**

**Min -> 0**

Example Usage:
    
    ...
    "game-settings": {
        "max-player-health":1, 
        ...
    }
    ...

---
### player-health-regenrate
*Double* that tells the game how much player can 'naturally' regenerate per second.

**Max -> *max-player-health***

**Min -> 0**

Example Usage:
    
    ...
    "game-settings": {
        "player-health-regenrate":0.125, 
        ...
    }
    ...

---
### map-size
Type: Int,

Information: Map Size (one side because map is square),


**Max -> 10000**

**Min -> 100**

If **Min** is too much for you, remember that you can just block the rest of map.

Example Usage:

    ...
    "game-settings": {
        "map-size":1000, 
        ...
    }
    ...

---
Thank you for reading ModManifest_DOCS.md
Here is snippet for you (Version: **0.0.1**):

    {
        "author":"",
        "title":"",
        "desc":"", 
        "short-desc":"",
        "game-settings": {
            "max-players": [Int here], 
            "min-players": [Int here],
            "max-player-health": [Int here],
            "player-health-regenrate": [Double Here], 
            "map-size": [Int here]
        }
    }