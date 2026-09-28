<div align="center">

# Explorer Tabs Manager

### Your File Explorer Tabs, **Always Restored.**

A lightweight Windows 11 utility that silently saves your open File Explorer tabs in the background and restores them when you reopen Explorer.

<br>

[![Windows 11](https://img.shields.io/badge/Windows%2011-22H2%2B-0078D4?style=flat-square&logo=windows11&logoColor=white)](https://www.microsoft.com/windows/windows-11)
[![.NET 8](https://img.shields.io/badge/.NET-8.0-512BD4?style=flat-square&logo=dotnet&logoColor=white)](https://dotnet.microsoft.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-00c875?style=flat-square)](LICENSE)
[![Open Source](https://img.shields.io/badge/Open%20Source-Yes-00ff88?style=flat-square)](https://github.com/Umair-Fareed/Explorer-Tabs-Manager)

<br>

<a href="https://suzagear.com/tabs">
  <img src="assets/download-installer.svg" alt="Download One-Click Installer">
</a>

<br>
<br>

**[Get the Installer](https://suzagear.com/tabs)** · **[Build from Source](#build-from-source)** · **[Features](#features)**

</div>

---

## Never lose your File Explorer workspace again

Windows 11 added tabs to File Explorer, but closing Explorer can still mean losing the collection of folders you had open.

**Explorer Tabs Manager** fixes that quietly.

It lives in the system tray, saves your current File Explorer tabs every few seconds, and brings them back automatically when Explorer is reopened. There are no pop-ups, no workflow interruptions, and no complicated setup.

> **Free & open source.** Every app feature is available in the source code under the MIT License.  
> If you would rather not build it yourself — or simply want to support development — you can get the ready-to-use **one-click installer** from [suzagear.com/tabs](https://suzagear.com/tabs).

---

## Features

| | Feature | What it does |
|---|---|---|
| 🔄 | **Auto-Save** | Saves all open File Explorer tabs automatically every few seconds. The default interval is 5 seconds and can be changed in Settings. |
| ⚡ | **Instant Restore** | Reopens your saved tabs automatically when File Explorer is opened again. |
| 🎯 | **Tray-Only UI** | Runs quietly in the Windows system tray. Right-click the tray icon whenever you need manual controls or Settings. |
| 💾 | **Manual Save & Restore** | Save the current tab session or restore it manually at any time from the tray menu. |
| 🛡️ | **No Clipboard Hacks** | Uses Windows UI Automation through FlaUI to open tabs natively instead of keyboard/clipboard tricks. |
| ⚙️ | **Configurable** | Change the save interval, toggle automatic restore, and optionally start the app with Windows. |
| 💻 | **Windows 11 Native** | Built specifically for the File Explorer tab system introduced in Windows 11 22H2+. |
| 🪶 | **Lightweight** | Runs as a separate background process and stays out of the way until you need it. |

---

## How it works

### 1. Run Explorer Tabs Manager

Start the app and it appears in your system tray. There is no configuration wizard or large window you need to keep open.

### 2. Work normally

Open File Explorer and use as many folders and tabs as you normally would. Explorer Tabs Manager saves the current tab session silently in the background.

By default, the session is saved every **5 seconds**.

### 3. Reopen File Explorer

Close File Explorer and open it again.

Explorer Tabs Manager detects the new Explorer window and restores your saved tabs automatically within a few seconds.

That's it.

---

## Get Explorer Tabs Manager

There are two ways to use the app. **Both contain the same features.**

### Option 1 — Build it yourself for free

The complete source code is available in this repository under the MIT License.

If you already have the .NET 8 SDK installed, you can clone the repository and run the app yourself.

**Cost:** Free  
**Best for:** Developers, open-source users, and anyone comfortable building a .NET project.

➡️ [Jump to the build instructions](#build-from-source)

### Option 2 — Get the one-click installer

If you do not want to install developer tools or build the project manually, a ready-to-use Windows installer is available from SUZA Gear.

The installer is a **paid convenience option** and a way to support continued development of the project. It does **not** unlock a separate feature set — the open-source build and installer version provide the same core app functionality.

<div align="center">

<a href="https://suzagear.com/tabs">
  <img src="assets/download-installer.svg" alt="Download One-Click Installer">
</a>

**[suzagear.com/tabs](https://suzagear.com/tabs)**

*One-time purchase · Ready-to-use installer · No development tools required*

</div>

---

## Build from source

### Requirements

- **Windows 11 22H2 or later**
- **.NET 8 SDK** or later
- **Git**
- Visual Studio 2022 or VS Code is optional — the project can be built from the command line

### Clone the repository

```powershell
git clone https://github.com/Umair-Fareed/Explorer-Tabs-Manager.git
cd Explorer-Tabs-Manager
```

### Restore dependencies

```powershell
dotnet restore
```

### Build

```powershell
dotnet build
```

### Run

```powershell
dotnet run --project ExplorerTabManager
```

Once launched, Explorer Tabs Manager will appear in the Windows system tray.

> If you prefer not to install the .NET SDK or build the project yourself, use the [one-click installer](https://suzagear.com/tabs).

---

## Using the app

### System tray menu

Right-click the Explorer Tabs Manager tray icon to access:

- **Save Tabs Now** — immediately save the tabs that are currently open
- **Restore Tabs Now** — manually restore your saved Explorer session
- **Settings** — configure automatic saving, restoring, and startup behavior
- **Exit** — close Explorer Tabs Manager

### Settings

You can configure:

- **Auto-Save** — automatically save open File Explorer tabs
- **Save interval** — choose how frequently the tab session is saved
- **Auto-Restore** — restore saved tabs when File Explorer is reopened
- **Start with Windows** — launch Explorer Tabs Manager automatically when you sign in

---

## What happens after a crash or restart?

Explorer Tabs Manager writes the saved tab session to disk every few seconds.

As long as a session has been saved, your tabs can be restored after Explorer closes, Windows restarts, or the system crashes. For automatic restoration after signing back into Windows, enable **Start with Windows**.

Saved session data is stored locally in:

```text
%AppData%\ExplorerTabManager\
```

---

## Safety & implementation

Explorer Tabs Manager is designed to work alongside File Explorer rather than modifying it.

- It does **not inject code into `explorer.exe`**
- It does **not modify Windows system files**
- It does **not rely on clipboard manipulation**
- It uses **Windows UI Automation via FlaUI** to open tabs
- It uses the **Shell.Application COM interface** when reading Explorer windows/tabs
- It runs as a separate process and only interacts with Explorer when needed

Because the project is open source, you can inspect the implementation directly in this repository.

---

## Compatibility

| Platform | Support |
|---|---|
| Windows 11 22H2+ | ✅ Supported |
| Windows 10 | ❌ Not supported |
| macOS | ❌ Not supported |
| Linux | ❌ Not supported |

Explorer Tabs Manager depends on the native File Explorer tab system introduced in **Windows 11 22H2 (Build 22621)**.

---

## Open source vs. installer

| | Build from Source | One-Click Installer |
|---|---:|---:|
| Full Explorer Tabs Manager functionality | ✅ | ✅ |
| Source code included | ✅ | — |
| MIT licensed source | ✅ | ✅ Project source |
| Requires .NET 8 SDK to build | ✅ | ❌ |
| Ready-to-run setup | ❌ | ✅ |
| Clean installer / uninstaller | ❌ | ✅ |
| Helps support continued development | — | ❤️ |
| Cost | **Free** | **Paid convenience option** |

The project is intentionally **open source first**. Paying is not required to access the app's features; the installer exists for people who prefer convenience and for anyone who wants to support the project.

---

## FAQ

### Does Explorer Tabs Manager restore tabs automatically?

Yes. When auto-restore is enabled, reopening File Explorer triggers restoration of the last saved tab session. You can also restore the session manually from the tray icon.

### How often are tabs saved?

The default auto-save interval is **5 seconds**. You can change the interval in Settings.

### Does it work on Windows 10?

No. File Explorer tabs are a Windows 11 feature, and Explorer Tabs Manager requires **Windows 11 22H2 or later**.

### Is the open-source version limited?

No. The source-code version includes the app's full functionality. The paid installer is a convenience option for users who do not want to install development tools and build the project manually.

### Does the app modify File Explorer?

No. It does not inject into `explorer.exe` or modify system files. It interacts with Explorer through Windows automation and shell APIs.

### Can I use the source version on multiple PCs?

Yes. The project is MIT licensed, so you can build and run the source version on your own machines.

---

## Contributing

Contributions are welcome.

If you find a bug, have an idea, or want to improve the project:

1. Fork the repository
2. Create a branch for your change
3. Make and test your changes
4. Open a Pull Request with a clear description

You can also open an Issue for bug reports and feature requests.

---

## Support the project

If Explorer Tabs Manager saves you time and you would like to support continued development, the easiest way is to get the ready-to-use installer from SUZA Gear.

<div align="center">

<a href="https://suzagear.com/tabs">
  <img src="assets/support-development.svg" alt="Support Explorer Tabs Manager">
</a>

<br>

**https://suzagear.com/tabs**

</div>

You can also help by starring the repository, reporting bugs, improving the documentation, or contributing code.

---

## License

Explorer Tabs Manager is open source under the **MIT License**.

See [LICENSE](LICENSE) for the full license text.

---

<div align="center">

Made by **SUZA**

[SUZA Gear](https://suzagear.com) · [Explorer Tabs Manager](https://suzagear.com/tabs)

</div>
