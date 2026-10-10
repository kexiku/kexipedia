*XDG Base Directory Specification* defines a range of standard [[environment variables]] where user-specific files should be found.

Many UNIX tools and applications utilize these variables by default.

## 👤 User directories

- `XDG_CONFIG_HOME`
    - User-specific configuration files (similar to `/etc`)
    - Default: `$HOME/.config`

- `XDG_CACHE_HOME`
    - Non-essential, cached data (similar to `/var/cache`)
    - Default: `$HOME/.cache`

- `XDG_DATA_HOME`
    - User-specific data files (similar to `/usr/share`)
    - Default: `$HOME/.local/share`

- `XDG_STATE_HOME`
    - User-specific state files, such as logs (similar to `/var/lib`)
    - Default: `$HOME/.local/state`

- `XDG_RUNTIME_DIR`
    - User-specific runtime files such as sockets, named pipes, etc.
    - Cleared on logout
    - Not required to have a default value
    - [[systemd]] sets this to `/run/user/$UID`

## 💽 System directories

- `XDG_CONFIG_DIRS`
    - List of directories separated by `:` (analogous to `PATH`)
    - Default to `/etc/xdg`

- `XDG_DATA_DIRS`
    - List of directories separated by `:` (analogous to `PATH`)
    - Default to `/usr/local/share:/usr/share`





[^1]: Sources:
		https://en.wikipedia.org/wiki/Freedesktop.org
