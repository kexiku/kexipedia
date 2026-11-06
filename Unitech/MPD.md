*Music Player Daemon* (*MPD*) is a flexible, lightweight [[Daemons|daemon]] for playing music on [[Linux]].

It can play audio files, organize playlists and maintain a music database.

## ⚙️ Config

MPD's config file can be located in various paths depending on the scope:

- `~/.config/mpd/mpd.conf` for per-user configuration
- `/etc/mpd.conf` for system-wide configuration

User configuration directory may not exists by default: it's recommended to create it explicitly:

```bash
mkdir -p ~/.config/mpd/mpd.conf
```

To build a user config, copy the example config file to your config directory:

```bash
cp /usr/share/doc/mpd/mpdconf.example.gz ~/.config/mpd/
gzip -d mpdconf.example.gz # Unzip if needed
mv mpdconf.example mpd.conf # Rename
```

You can use it as a starting point to create your own config.

## 🛠️ Setup

- Create all the directories you've manually pointed to in config file:

```bash
mkdir -p <playlist_dir>
mkdir -p <state_dir>
```

- Enable MPD as user service:

```bash
systemctl --user enable mpd.service
```

## 🔉 Outputs

By default, no audio outputs are configured, which leads MPD to use [[ALSA]] as a fallback.

To play audio using modern sound servers such as [[PulseAudio]] or [[PipeWire]], you should uncomment the corresponding sections in config file.





---

<small>Sources:</small>
<small>• https://wiki.archlinux.org/title/Music_Player_Daemon</small>
<small>• https://mpd.readthedocs.io/en/stable/user.html#</small>
