*Flatpak* is a universal software deployment and package management framework for Linux that allows applications to run in a secure, isolated environment.

Packages distributing via Flatpak are called *flatpaks*.

Unlike traditional package formats which targets specific OS, flatpaks target specific *runtimes*.
A Flatpak runtime provides the required libraries and other dependencies, which can then be shared across different flatpaks.

All Flatpak applications are *sandboxed*, which means they are isolated from the host and other applications.
That ensures high security and stability of the system.

## ✅ Main advantages of flatpaks

- No dependency conflicts
- Run on most Linux distros
- Don't require administrative privileges
- Keep bugs isolated so system files remain untouched
- Save disk space by reusing dependencies

## 🛠️ Installation

See https://flathub.org/en/setup



[^1]: Sources:
	https://docs.flatpak.org/en/latest/basic-concepts.html
	https://fedoraproject.org/wiki/Flatpak