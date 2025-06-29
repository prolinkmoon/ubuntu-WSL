# Install Ubuntu on WSL (Windows Subsystem for Linux)

This guide walks you through installing **Ubuntu WSL** on Windows 10/11. WSL allows you to run Linux directly on Windows without the need for a virtual machine.

---

## 🖥️ Requirements

- Windows 10 version 2004+ (Build 19041+) or Windows 11
- Admin privileges
- Internet connection

---

## ⚙️ Step-by-Step Installation

### 1. Enable WSL & Virtual Machine Platform

Open **PowerShell as Administrator** and run:

```powershell
wsl --install
```

Or, manually enable features:
```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```
Then reboot your computer.

### 2. Set WSL2 as Default (Optional but Recommended)
```powershell
wsl --set-default-version 2
```
### 3. Install Ubuntu from Microsoft Store
1. Open the Microsoft Store
2. Search for `Ubuntu` (e.g., Ubuntu 22.04 LTS)
3. Click Install

### 4. Launch Ubuntu
After installation:
- Open Ubuntu from the Start Menu
- Wait for setup (may take a few minutes)
- Create your Linux username and password

---

## 🧪 Verify Installation
```powershell
wsl --list --verbose
```
Expected output:
```powershell
NAME      STATE           VERSION
Ubuntu    Running         2
```

## 🧰 Common Commands
- Launch Ubuntu: wsl or search “Ubuntu” in Start Menu
- Shut down WSL: `wsl --shutdown`
- Update Ubuntu: `sudo apt update && sudo apt upgrade`

## 🛠️ Troubleshooting
- [WSL official docs](https://learn.microsoft.com/en-us/windows/wsl/)
- [Ubuntu on WSL Docs](https://ubuntu.com/desktop/wsl)
- Reset Ubuntu: `wsl --unregister Ubuntu` (⚠️ deletes all data)
- Check Windows version: winver





