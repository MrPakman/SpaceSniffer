# Hide Custom Commands - Skript Installation Guide

## Description

This Skript hides all non-vanilla (custom/plugin) commands from tab completion in Minecraft servers. Players will only see vanilla Minecraft commands when pressing Tab.

## Files Included

1. **hide-custom-commands.sk** - Basic version that hides all custom commands
2. **hide-custom-commands-advanced.sk** - Advanced version with permission bypass support
3. **README-SKRIPT.md** - Detailed documentation (Russian)
4. **USAGE-EXAMPLES.md** - Usage examples and FAQ (Russian)
5. **INSTALLATION.md** - This file

## Quick Start

### Prerequisites
- Minecraft Server (Spigot/Paper/Purpur)
- Skript plugin version 2.6 or higher
- Java Edition 1.16+

### Installation Steps

1. **Download Skript** (if not already installed)
   - Get it from: https://github.com/SkriptLang/Skript/releases
   - Place the Skript.jar in your `plugins/` folder
   - Restart the server

2. **Choose a version**
   - **Basic version**: `hide-custom-commands.sk` - Hides commands for everyone
   - **Advanced version**: `hide-custom-commands-advanced.sk` - Allows admins to see all commands

3. **Install the script**
   - Copy the chosen `.sk` file to `plugins/Skript/scripts/`
   - Run command: `/skript reload hide-custom-commands`
   - Or restart the server

4. **Done!** Custom commands are now hidden from tab completion

## Basic Version Features

- Hides all non-vanilla commands from tab completion
- Simple and lightweight
- Works for all players
- No configuration needed

## Advanced Version Features

- Hides custom commands for regular players
- Admins with permission can see all commands
- Includes `/toggletab` command to switch modes
- Configurable via permissions

### Permissions (Advanced Version)

- `tabcomplete.bypass` - See all commands (not just vanilla)
- `tabcomplete.toggle` - Use /toggletab command

### Commands (Advanced Version)

- `/toggletab` - Toggle between seeing all commands or just vanilla commands

## Customization

### Adding Commands to Whitelist

1. Open the `.sk` file in a text editor
2. Find the `options:` section at the top
3. Add your command to the `vanilla-commands` list

Example:
```yaml
options:
    vanilla-commands: "help", "give", "gamemode", "mycustomcommand"
```

### Removing Commands from Whitelist

Simply remove the command from the `vanilla-commands` list.

## Vanilla Commands Included

The script includes all vanilla Minecraft commands such as:
- Administrative: ban, kick, op, deop, etc.
- Gameplay: gamemode, give, teleport, etc.
- World: worldborder, setblock, fill, etc.
- System: save-all, stop, reload, etc.

Full list is in the script file (approximately 70+ commands).

## How It Works

1. Script intercepts the `tab complete` event
2. Gets the list of suggested completions
3. Filters out all non-vanilla commands
4. Returns only vanilla commands to the player

## Important Notes

- Commands can still be used by typing them manually
- This does NOT affect command permissions
- This only hides commands from tab completion
- Players can still execute custom commands if they know the name

## Testing

After installation, test by:
1. Press Tab in chat to see command suggestions
2. Try typing `/sk` and press Tab (Skript commands should be hidden)
3. Try typing `/help` and press Tab (should show vanilla help command)

## Troubleshooting

### Commands still visible
- Check script is loaded: `/skript list`
- Reload the script: `/skript reload hide-custom-commands`
- Check for errors: `/skript info hide-custom-commands`

### Script not loading
- Verify Skript version 2.6 or higher
- Check server console for errors
- Ensure file is in correct folder: `plugins/Skript/scripts/`

### Some vanilla commands not working
- Update the vanilla commands list for your Minecraft version
- Check Skript version compatibility

## Compatibility

### Tested On
- Minecraft 1.16.5 - 1.20.x
- Paper, Spigot, Purpur servers
- Skript 2.6+

### Works With
- All Minecraft plugins
- Any server software (Spigot-based)
- Any Minecraft version 1.16+

## Performance

- Minimal impact on server performance
- Only runs when players press Tab
- Lightweight command filtering
- No database or storage requirements

## Support

If you encounter issues:
1. Check the Troubleshooting section above
2. Verify all prerequisites are met
3. Check server logs for errors
4. Update Skript to latest version

## License

Free to use for any purpose.

## Version History

- v1.0 - Initial release with basic and advanced versions
- Full vanilla command list for Minecraft 1.19+
- Russian and English documentation

## Credits

Created to hide custom commands from tab completion in Minecraft servers using the Skript plugin.
