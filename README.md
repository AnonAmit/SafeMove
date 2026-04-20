# SafeMove  🚀

SafeMove is an intelligent file management utility designed to safely move applications (e.g., from `C:` to `D:`) without breaking them. It uses **Windows Directory Junctions** (`mklink /J`) and robust `robocopy` operations to ensure data integrity and seamless redirection.

# UI
<img src="ui.png" width="300" />

## Key Features

- **🛡️ Safe Move**: Uses `robocopy` for atomic moves and verifies data integrity before deleting source files.
- **🔗 Seamless Redirection**: Creates NTFS Junctions so Windows and apps think files are still in the original location.
- **🧠 AI Powered**: Optional integration with LLMs (Cloud or Local/Ollama) to give advice on what is safe to move.
- **🚫 Safety Rules**: Automatically prevents moving critical system folders (Windows, System32) and detects already moved items (Junctions).
- **🎨 Cyberpunk Theme**: Built-in Theme Engine with "Standard" and "Cyberpunk" (Neon) modes.
- **📊 Disk Dashboard**: Visualizes your C: Drive health and space reclamation potential.

## Installation

### Binary (Portable)
1. Download `SafeMoveAI_Portable.zip` from Releases.
2. Extract to any folder.
3. Run `SafeMoveAI.exe`.

### From Source
Requirements: Python 3.11+
```bash
git clone https://github.com/yourusername/SafeMoveAI.git
cd SafeMoveAI
pip install -r requirements.txt
python main.py
```

## Usage

1. **Scan**: Click **Scan C: Drive** to list installed apps and large folders in AppData.
2. **Review**: Check the **Status** column.
    - 🟢 **SAFE**: Safe to move (e.g., Spotify, Chrome Data).
    - 🔴 **FORBIDDEN**: System files or critical paths.
    - ⚪ **MOVED**: Already moved (Junction detected).
3. **Plan**: Switch to **Plan & Move** tab. Select the apps you want to move.
4. **Move**: Click **Execute Move Plan**.
    - *Note: Requires Administrator Privileges.*


## Disclaimer
Always backup critical data before performing bulk file operations. While SafeMove AI uses industry-standard safe methods (`robocopy`), I am not responsible for data loss.

