*PipeWire* is a modern low-level multimedia framework for hanlding audio and video streams on [[Linux]].

It's designed as a successor to older [[sound servers]] like [[PulseAudio]] and [[JACK]], aiming to unify audio and video processing by providing minimal latency and playback functionality.

PipeWire uses [[WirePlumber]] as its standard session manager to handle stream routing.

## 🪛 Troubleshooting

If audio stream is not playing, try resetting WirePlumber’s saved state:

```bash
# Stop wireplumber service
systemctl --user stop wireplumber

# Backup the state directory
mv ~/.local/state/wireplumber ~/.local/state/wireplumber.bak

# Restart wireplumber service
systemctl --user start wireplumber
```

PipeWire will recreate the persistent state directory on startup.

If the state resetting didn't help, you can try to reset WirePlumber to default state by removing its config files:

```bash
# Remove WirePlumber config only
wpctl reset

# Optionally remove PipeWire config and restart the PipeWire service
wpctl reset -a
```





[^1]: Sources:
		https://en.wikipedia.org/wiki/PipeWire
		https://wiki.archlinux.org/title/PipeWire
	
