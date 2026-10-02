In Linux, each device is represented as a [[files|file]] located in the `/dev` directory.

There are 3 types of device files:
## [c] Character devices

- Transfer data character-by-character without a buffer
  (keyboards, mice, serial ports)

## [b] Block devices

- Transfer data in blocks using a buffer
  (HDD, SSD, USB drives etc.)

## 🫥 Pseudo-devices

- Virtual devices with no physical counterpart
  (`/dev/random`, `/dev/null`)

## 💽 Device naming convention

```
 ╭──────────────────────────────────────────────────────────────────────────╮
 │ DEVICE                        │ FILE NAME                                │
 │┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈ ✧ ┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈│
 │ ★ Hard Disks                  | /dev/sd*                                 │
 │ ★ Virtual Disks               | /dev/vd*, /dev/xvd*                      │
 │ ★ Non-Volatile Memory Devices | /dev/nvme*                               │
 │ ★ Device Mapper               | /dev/dm-*, /dev/mapper/*                 │
 │ ★ CD and DVD Drives           | /dev/sr*                                 │
 │ ★ PATA Hard Disks             | /dev/hd*                                 │
 │ ★ Terminals                   | /dev/tty*, /dev/pts/*, /dev/tty          │
 │ ★ Serial Ports                | /dev/ttyS*, /dev/ttyUSB*, /dev/ttyACM*   │
 │ ★ Parallel Ports              | /dev/lp0 and /dev/lp1                    │
 │ ★ Audio Devices               | /dev/snd/*, /dev/dsp, /dev/audio         │
 ╰──────────────────────────────────────────────────────────────────────────╯
```





[^1]: Sources:
	https://opensource.com/article/16/11/managing-devices-linux
	https://wiki.archlinux.org/title/Device_file
