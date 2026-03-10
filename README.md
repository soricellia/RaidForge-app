# RaidForge

A desktop tool for Raid: Shadow Legends that reads your account data directly from the running game and exports it as structured JSON. Built for players who want full visibility into their roster, gear, and spending — without relying on screenshots or manual entry.

## What It Does

RaidForge attaches to a running instance of Raid: Shadow Legends in **read-only mode** and extracts:

| Domain | Data |
|--------|------|
| **Heroes** | Full roster with stats, skills, masteries, blessings, and equipped gear |
| **Artifacts** | Complete artifact inventory with sets, substats, and enhancement levels |
| **Account** | Player level, power, resources, gems, and shard counts |
| **Payments** | Purchase history totals and subscription records |

All data is saved locally as JSON files. Nothing is uploaded, modified, or sent anywhere.

## Download

**[Download the latest release](https://github.com/soricellia/RaidForge-app/releases/latest)**

1. Download the `.zip` file from the link above.
2. Extract it anywhere on your computer.
3. Run **RaidForge.App.exe**.

No .NET installation required — the download is fully self-contained.

## Requirements

- Windows 10 or 11 (64-bit)
- Raid: Shadow Legends running and logged in (past the title screen)
- May require running as Administrator depending on your system

## How to Use

1. Launch Raid: Shadow Legends and log into your account.
2. Open **RaidForge.App.exe**.
3. Your account will appear in the list automatically. If you run multiple game clients, each account shows up by name and level.
4. Select the account you want and click **Extract Data**.
5. When it finishes, click **Open Output Folder** to find your JSON files.

## Output

Each extraction produces:

```
output/
├── index.json        # Summary manifest
├── heroes.json       # Full hero roster with stats, skills, masteries
├── artifacts.json    # Every artifact with sets, substats, rolls
├── account.json      # Level, power, resources, gems, shards
└── payments.json     # Purchase totals, subscription records
```

Every file includes metadata (game version, extraction timestamp) and can be used independently.

## Is This Safe?

RaidForge is strictly **read-only**. It does not:

- Write to or modify game memory
- Inject code, DLLs, or hooks into the game
- Send any network traffic
- Modify any game files on disk
- Run anything inside the game process

The tool opens the game with read-only access and can be closed at any time with zero impact on the game.

## Troubleshooting

| Problem | Solution |
|---------|----------|
| "No game detected" | Make sure Raid is running and you're past the login screen. |
| "Failed to attach" | Right-click RaidForge and select **Run as Administrator**. |
| "AppModel not found" | The game is still loading. Wait until you're on the main screen and try again. |
| "Game build mismatch" warning | The game was recently updated. RaidForge may need an update to match — check back for a new release. |

## License

This project is for personal, educational use only. Use at your own discretion.
