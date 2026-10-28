*ALSA* (*Advanced Linux Sound Architecture*) is the core sound framework built in the [[Kernel|Linux kernel]].

It provides drivers and API for sound cards to handle audio input/output, serving as the base layer for [[sound servers]] like [[PulseAudio]] and [[PipeWire]].

ALSA consists of two main components: kernel-level device drivers that manage the hardware, and a user-space library (`alsa-lib`) that allows application developers to interact with those drivers without needing to write low-level code.

By default, ALSA only allows a single application at a time to access a sound card; thus, it **cannot** mix audio output from multiple streams.





[^1]: Sources:
		https://wiki.archlinux.org/title/Advanced_Linux_Sound_Architecture
