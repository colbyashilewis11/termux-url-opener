# Termux URL-Opener for yt-dlp

A simple interactive downloader script for Termux.
This script works as a Termux URL-Opener and provides an interactive way to download videos using yt-dlp.

For details about how Termux handles URL sharing and hooks, see:  
https://wiki.termux.com/wiki/Intents_and_Hooks

---

## Features

* Works as a Termux URL-Opener (Share → Termux)
* Displays the full format list using `yt-dlp -F`
* Accepts real format codes directly from the user
* Provides shortcut commands for common format selections
* Designed for interactive manual operation

---

## Requirements

* Termux
* Python
* yt-dlp
* ffmpeg


---

## Installation

Copy the script to:
```
    $HOME/bin/termux-url-opener
```
Make it executable:
```sh
    chmod +x $HOME/bin/termux-url-opener
```
Exit Termux (or restart it).

---

## Usage

Share a video URL to Termux from your browser or another app.  
The script will display available formats using `yt-dlp -F`.

Enter either:
A format code from the list  
Or one of the shortcut commands below.
```
    -y   / --yt720      : 720p with audio (YouTube)
    -e   / --yt720en    : 720p with English audio (YouTube)
    -m   / --mp4-720    : 720p or lower (mp4)
    -u   / --uni720     : 720p or lower (universal)
    -d   / --default    : default format (without -f option)
```
You may also directly enter any format code shown by `yt-dlp -F` (or `--list-formats`).

---

## Notes

* Entering a format code shown by `-F` uses that format directly.
* Shortcut commands are provided only for convenience.
* This script intentionally performs no validation on format input.

---

## Design Philosophy

This tool is intentionally simple and transparent.
All format decisions are controlled by the user.
The script only assists in expanding shortcuts and executing yt-dlp.