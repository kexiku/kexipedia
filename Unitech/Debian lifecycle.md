[[Debian]] follows a 2-year release cycle for major versions, with each release typically supported for a 5-year total lifetime.

## 🌱 Release stages

Before becoming available in [[Debian releases|Stable]] repository, every Debian software package goes through a full release workflow, which consists of four distinct stages:

### 1. Sid

- The primary destination for newly uploaded packages
- At this stage, the software is developing actively and may contain bugs or cause breaking changes

### 2. Testing

- Packages migrate to [[Debian releases|Testing]] when they meet certain criteria, such as dependency consistency and the absence of critical bugs

### 3. Freeze

- Before releasing a package, Debian gradually restricts changes by freezing it
- The focus shifts from adding features to fixing bugs
- Lasts about 7 ± 1 months before getting released

### Stable release

- Once the release is ready, Testing becomes the new Stable, receiving a version number and codename
- The previous Stable release becomes Oldstable, and a new Testing branch is created for the next release





[^1]: Sources:
		https://wiki.debian.org/DebianReleases
