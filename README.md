# Explorer Tab Manager

A lightweight system tray application for Windows 11 that provides persistent tab management for File Explorer.

## Features

- 🔄 **Auto-Save & Restore**: Automatically save your Explorer tabs and restore them when you reopen Explorer
- ⚡ **Quick Access**: System tray icon for easy access to save/restore functions
- ⌨️ **Hotkeys**: Customizable keyboard shortcuts for saving and restoring tabs
- ⚙️ **Configurable**: Set default tab locations, auto-save intervals, and more
- 🚀 **Lightweight**: Minimal resource usage, runs silently in the background

## Why This Project?

Windows 11 introduced native tabs for File Explorer, but lacks the ability to:
- Restore tabs after accidentally closing Explorer
- Set a custom default location for new tabs
- Persist tabs between sessions (without logging out)

This tool fills that gap, similar to how QTTabBar worked on Windows 10.

## Installation

1. Download the latest release from the [Releases](https://github.com/yourusername/ExplorerTabManager/releases) page
2. Extract and run `ExplorerTabManager.exe`
3. The app will appear in your system tray
4. Right-click the tray icon to access settings

## Usage

### System Tray Menu
- **Save Tabs**: Manually save all current Explorer tabs
- **Restore Tabs**: Restore previously saved tabs
- **Settings**: Configure the application
- **Exit**: Close the application

### Settings
- **Default Tab Location**: Set where new tabs should open
- **Auto-Save**: Enable automatic saving at specified intervals
- **Auto-Restore**: Automatically restore tabs when the app starts
- **Start with Windows**: Launch the app on system startup
- **Hotkeys**: Customize keyboard shortcuts (coming soon)

## Building from Source

### Prerequisites
- .NET 8.0 SDK or later
- Visual Studio 2022 (or VS Code with C# extension)

### Build Steps
```bash
git clone https://github.com/yourusername/ExplorerTabManager.git
cd ExplorerTabManager
dotnet build
dotnet run --project ExplorerTabManager
```

## Roadmap

- [ ] Global hotkey support
- [ ] Multiple tab profile management
- [ ] Custom new tab button behavior
- [ ] Tab grouping and organization
- [ ] Import/export tab configurations
- [ ] Better Windows 11 native tab integration

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

Inspired by QTTabBar and the need for better tab management in Windows 11 File Explorer.
