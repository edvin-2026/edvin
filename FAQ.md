# Frequently Asked Questions

**Q: Which version of Python should I install?**
A: Install the latest stable Python 3.x release from [python.org](https://www.python.org/downloads/). Avoid Python 2, which has been officially unsupported since January 2020.

**Q: Do I need to install pip separately?**
A: No. Since Python 3.4, pip is included automatically with the standard installer. You may need to run `python -m ensurepip --upgrade` if it's missing.

**Q: Can I have multiple versions of Python installed at the same time?**
A: Yes. This is common practice. Use a tool like `pyenv` (macOS/Linux) or the Windows `py` launcher to manage and switch between versions.

**Q: What's the difference between `python` and `python3` commands?**
A: On many macOS and Linux systems, `python` may point to Python 2 (if present) or may not exist at all, while `python3` explicitly points to a Python 3 installation. Windows installations typically only add `python`.

**Q: Do I need administrator/root access to install Python?**
A: For a system-wide installation, yes. However, you can install Python for a single user without elevated permissions by choosing a user-level install option or using a version manager like `pyenv`.

**Q: How do I update Python to a newer version?**
A: Download the newer installer from python.org and run it — it will typically upgrade your existing installation. On Linux, use your package manager (e.g., `sudo apt upgrade python3`).

**Q: How do I uninstall Python?**
A: 
- **Windows:** Use "Add or Remove Programs" in Settings.
- **macOS:** Remove the framework from `/Library/Frameworks/Python.framework` (advanced) or use the uninstaller if provided.
- **Linux:** Use your package manager, e.g., `sudo apt remove python3`.

**Q: Should I use Anaconda instead of the standard Python installer?**
A: Anaconda is a popular alternative distribution bundled with data science libraries and its own package manager (`conda`). It's a good choice if you're focused on data science, but the standard installer is lighter-weight and sufficient for general-purpose use.

**Q: What code editor should I use with Python?**
A: Python ships with IDLE, a basic editor. For more features, popular free options include Visual Studio Code and PyCharm Community Edition.

**Q: Where can I get help if something goes wrong?**
A: See the **Troubleshooting** section in `Installation.md`, or consult the official documentation at [docs.python.org](https://docs.python.org/3/).