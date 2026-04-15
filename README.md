# Godot Debug Menu

A collective of useful  functions and debug menu for real-time debugging in Godot 4.

![Debug Menu](readme/Screenshot%202026-04-15%20at%204.46.30%E2%80%AFPM.png)
![Code Example](readme/Screenshot%202026-04-15%20at%204.44.55%E2%80%AFPM.png)
![Console](<readme/Screenshot 2026-04-15 at 5.01.43 PM.png>)

## Features

- **Customizable Debug Menu**: Easily add custom buttons and actions.
- **Live-Updating Text**: Monitor performance metrics or any variable in real-time.
- **Rich Console Logs**: Timestamp, colors and >>**hyperlinks to source code**<<.
- **Auto-Disable**: Automatically disables in production builds for zero overhead.

## Hotkeys

- **\[F1]**: Toggle Debug Menu visibility.
- **\[F2]**: Take a screenshot (saved to `user://screenshots`).
- **\[F3]**: Pause/Unpause the game.

## Installation

- Download to your projects, verify the path:`<root>/addons/debug`
- Enable via Project Settings > Plugins > GodotDumdum's Debug Menu > Check "Enable"

## Usable Functions

```gdscript
# Logging
Debug.log(...messages)      # Print a standard log message.
Debug.warn(...messages)     # Print a yellow message.
Debug.error(...messages)    # Print an red message.
Debug.verbose(...messages)  # Print a gray debug message.

# Live Information
Debug.register_live(key, callback) # Register a function to display real-time info.
Debug.unregister_live(key)         # Remove a live-updating info item.

# ADd Menu Items
Debug.add_menu_item(text, function, arguments) # Add a custom action to the debug menu.
Debug.add_separator(text)                      # Add a separator or group header to the menu.

# Dialogs
Debug.dialog_input(title, callback, description, default)    # Show an input dialog.
Debug.dialog_confirm(title, description, on_confirm, on_cancel) # Show a confirmation dialog.

# Utilities
Debug.take_screenshot() # Capture and save a screenshot to the user folder.
Debug.time(id)          # Measure t the elapsed time between two calls with the same ID.
```

