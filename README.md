# HTV

![build](https://github.com/linuxmint/hypnotix/actions/workflows/build.yml/badge.svg)

**HTV** is a lightweight and improved fork of [Hypnotix](https://github.com/linuxmint/hypnotix), the IPTV player originally developed by Linux Mint.
This fork focuses on performance and usability improvements.

## Key Differences from the Original Hypnotix

- MPV is initialized only once
- Channel name is displayed as overlay text in the MPV player
- **Press Space** to pause or resume playback
- **Improved channel switching** with index-based wrap-around logic
- **Control volume** with the Up/Down arrow keys
- **Automatically scrolls to the active channel** in the list view
- **Merged** [PR #375 from linuxmint/hypnotix](https://github.com/linuxmint/hypnotix/pull/375):
  - Removed unused code and assets
  - Simplified and cleaned up the UI code
  - Potentially improved startup performance by reducing asset loading
- **Removed** the `circle-flags-svg` dependency to avoid installation issues on Debian
- **Volume is now preserved** when switching between channels
---

Hypnotix is an IPTV streaming application with support for live TV, movies and series.

![shadow](https://user-images.githubusercontent.com/1138515/99553152-b8bac780-29b5-11eb-9d75-8756ed7581b6.png)

It can support multiple IPTV providers of the following types:

- M3U URL
- Xtream API
- Local M3U playlist

# License

- Code: GPLv3
- Flags: https://github.com/linuxmint/flags
- Icons on the landing page: CC BY-ND 2.0

# Requirements

- libxapp 2.6+
- libmpv
- python3-imdbpy (for Older Mint and Debian releases get it from https://packages.ubuntu.com/focal/all/python3-imdbpy/download)
- circle-flags (https://github.com/linuxmint/circle-flags)

# TV Channels and media content

Hypnotix does not provide content or TV channels, it is a player application which streams from IPTV providers.

By default, Hypnotix is configured with one IPTV provider called Free-TV: https://github.com/Free-TV/IPTV.

This provider was chosen because it satisfied the following criterias:

- It only includes free, legal, publicly available content
- It groups TV channels by countries
- It doesn't include adult content

Issues relating to TV channels and media content should be addressed directly to the relevant provider.

Note: Feel free to remove Free-TV from Hypnotix if you don't use it, or add any other provider you may have access to or local M3U playlists.

# Wayland compatibility

If you're using Wayland go the Hypnotix preferences and add the following to the list of MPV options:

`vo=x11`

Run Hypnotix with:

`GDK_BACKEND=x11 hypnotix`
