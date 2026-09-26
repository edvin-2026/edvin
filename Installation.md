# Python Installation Guide

## Software Requirements

Before installing Python, make sure your system meets the following requirements:

| Requirement | Details |
|---|---|
| Operating System | Windows 10/11, macOS 11+, or a modern Linux distribution |
| Disk Space | At least 100 MB free (more if installing additional packages) |
| RAM | 2 GB minimum recommended |
| Internet Connection | Required to download the installer and packages |
| Administrator/Root Access | Recommended for a system-wide installation |

You will also need a web browser to download the installer from the official source: [python.org/downloads](https://www.python.org/downloads/).

---

## Installation Steps

### Windows

1. Go to [python.org/downloads](https://www.python.org/downloads/) and download the latest stable Windows installer (64-bit recommended).
2. Run the downloaded `.exe` file.
3. **Important:** On the first installer screen, check the box labeled **"Add python.exe to PATH"**.
4. Click **Install Now** for the default installation, or **Customize installation** to choose specific features and an install location.
5. Wait for the installation to complete, then click **Close**.

### macOS

1. Go to [python.org/downloads](https://www.python.org/downloads/) and download the latest macOS installer (`.pkg` file).
2. Open the downloaded file and follow the installer prompts.
3. Enter your administrator password when requested.
4. Once complete, open **Terminal** to confirm the installation (see Verification Steps below).

Alternatively, if you use [Homebrew](https://brew.sh/), you can install Python with:
```bash
brew install python3
```

### Linux (Debian/Ubuntu-based)

Most Linux distributions include Python by default, but you can install or update it manually:

```bash
sudo apt update
sudo apt install python3 python3-pip
```

### Linux (Fedora/RHEL-based)

```bash
sudo dnf install python3 python3-pip
```

---

## Verification Steps

After installation, confirm that Python is installed and accessible from the command line.

1. Open a terminal or command prompt:
   - **Windows:** Command Prompt or PowerShell
   - **macOS/Linux:** Terminal
2. Run the following command:
   ```bash
   python --version
   ```
   or, on some systems:
   ```bash
   python3 --version
   ```
3. You should see output similar to:
   ```
   Python 3.12.4
   ```
4. Verify that `pip` (the package manager) is also installed:
   ```bash
   pip --version
   ```
5. Optionally, launch the interactive interpreter to confirm everything works:
   ```bash
   python
   >>> print("Hello, Python!")
   ```
   Type `exit()` to leave the interpreter.

---

## Troubleshooting

### "python is not recognized as an internal or external command" (Windows)
- This usually means Python was not added to your system PATH during installation.
- **Fix:** Re-run the installer, choose **Modify**, and ensure **"Add python.exe to PATH"** is checked. Alternatively, add the Python install directory manually to your system's Environment Variables.

### "command not found: python" (macOS/Linux)
- Many systems use `python3` instead of `python` by default.
- **Fix:** Try `python3 --version` instead, or create an alias:
  ```bash
  alias python=python3
  ```

### Multiple Python Versions Conflicting
- If you have several versions installed, the wrong one may run by default.
- **Fix:** Use `py -0` (Windows) or `which -a python3` (macOS/Linux) to list installed versions, and use the full version-specific command (e.g., `python3.12`) when needed.

### pip Not Found or Not Working
- **Fix:** Reinstall pip using:
  ```bash
  python -m ensurepip --upgrade
  ```

### Permission Errors During Installation (Linux/macOS)
- **Fix:** Run the install command with `sudo`, or install Python in a user-level directory using a version manager like `pyenv`.

### Installer Freezes or Fails Midway (Windows)
- **Fix:** Disable antivirus software temporarily, ensure you have enough disk space, and re-download the installer in case the original file was corrupted.

If a problem persists, check the **FAQ.md** file or consult the official documentation at [docs.python.org](https://docs.python.org/3/using/index.html).