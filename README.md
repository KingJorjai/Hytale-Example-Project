# Hytale Plugin Template

Personal VS Code template for Hytale plugin development.

## Requirements

- Hytale (Flatpak)
- VS Code + Java Extension Pack
- Java 25

## Quick Start

1. Update `settings.gradle` - Set project name
2. Update `gradle.properties` - Set `maven_group` and `version`
3. Update `src/main/resources/manifest.json` - Set plugin metadata and `Main` class
4. Press `F5` to run and debug
5. First run: `/auth login device` in server console

## Development

- **Run/Debug**: Press `F5` in VS Code
- **Build JAR**: `./gradlew build` (output in `build/libs/`)
- **Connect**: Local Server or `127.0.0.1` in Hytale client
- **Debugging**: Set breakpoints, they work automatically
- **Server files**: Everything runs in `./run/` (git-ignored)

## Configuration

The template auto-updates `Version` and `IncludesAssetPack` in manifest.json based on gradle.properties.

Hytale path configured for Linux Flatpak in `build.gradle`. Change if needed:
- Linux Flatpak: `~/.var/app/com.hypixel.HytaleLauncher/data/Hytale`
- Windows: `~/AppData/Roaming/Hytale`
- macOS: `~/Library/Application Support/Hytale`

## Example Plugin

Includes example command `/test` and dirt crafting recipe. Remove before production.