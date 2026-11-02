---
banner: wimblows.webp
banner_icon: 🗿
cssclasses:
  - dashboard
obsidianUIMode: preview
---
- Utilities
	- [[diskpart]]
	- [[chkdsk]]
	- [[Windows Recovery Environment]]

## 💽 Disable automatic driver updates

1. Open Group Policy Editor (`gpedit.msc`)
2. Go to:
	- Computer configuration
	- Administrative Templates
	- Windows Components
	- Windows Update
	- Manage updates offered from Wimblows Update
3. Set `Do not include drivers with Windows Updates` to `Enabled`