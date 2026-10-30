[[Debian]] comes in different release options ( officially called *distributions*) which serves a variety of users needs.

There are three major release channels: **Stable**, **Testing** and **Unstable**, also known as **Sid**.

## Overview

### 🔬 Stable

- Actually stable
- Good for beginners
- Amazing for servers
- Has full security support

### 🧪 Testing

- Has more up-to-date software than Stable
- Breaks less often than Unstable

### 🥽 Unstable

- Has the latest software
- Suitable for experienced users
- More prone to bugs and breakages

## Stable

At any given time, there is only *one* Stable release of Debian.

Security updates are provided by Debian security team for *3 years*.
This generally means that each Stable release is supported for its whole life plus an extra year after a new version of stable is released.

An extended security support up to *5 years* total is available in the [[Debian LTS]] release.

> [!tip]
> Codenames for all the stable versions of Debian are taken from the ["Toy Story"](https://disney.fandom.com/wiki/Toy_Story_(franchise)) franchise by Pixar: each version named by a toy character from the movie.

## Testing

In *Testing* things should not break as badly as in Unstable, because packages are allowed to enter testing only after a certain period of time has passed to make sure that they don't have any critical bugs filed against them.

## Unstable

*Sid*, or *Unstable*, is the place where most of the packages are initially uploaded.

It will never be released directly, because packages which are to be released will first have to be included in *Testing*, in order to be included in *Stable* later on.

The name "Sid" also comes from the "Toy Story" animated motion picture: Sid was the boy next door who destroyed toys :)

> [!warning]
> Changing the release channel is possible, but it's a one way process.
> 
> You can go from Stable → Testing → Unstable, but the reverse direction is **not** possible. Think twice if you are planning to upgrade to testing or unstable.





[^1]: Sources:
		https://www.debian.org/doc/manuals/debian-faq/choosing.en.html
		https://www.debian.org/doc/manuals/debian-faq/ftparchives.en.html#dists
		https://wiki.debian.org/Debian_Systems_Administration_for_non-Debian_SysAdmins