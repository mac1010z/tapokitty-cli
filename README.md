# tapokitty-cli

Control Tapo cameras from the terminal with **high-quality Kitty graphics protocol** rendering. Full resolution live streaming directly in your terminal.

> Requires a [Kitty](https://sw.kovidgoyal.net/kitty/)-compatible terminal. For a version that works in any terminal (using half-block characters), see [tapo-cli](https://github.com/mac1010z/tapo-cli).

## Install

```bash
brew install mac1010z/tools/tapokitty-cli
```

## Setup

On first run, a config file is created at `~/.config/tapo-cli/config.json` (shared with tapo-cli):

```json
{
  "cameras": {
    "living": {"ip": "192.168.1.100", "name": "Living Room"},
    "door": {"ip": "192.168.1.101", "name": "Front Door"}
  },
  "rtsp_user": "your_rtsp_user",
  "rtsp_password": "your_rtsp_password",
  "api_user": "admin",
  "api_password": "your_api_password"
}
```

## Requirements

- `ffmpeg`
- A **Kitty-compatible terminal** (Kitty, WezTerm, etc.)

## Usage

```bash
tapokitty list                    # List configured cameras
tapokitty view living             # HD live stream
tapokitty snap living             # Terminal snapshot
tapokitty status living           # Show camera info
tapokitty privacy living on       # Cover the lens
tapokitty move living 10 0        # Pan right
tapokitty guide                   # Show setup guide
```

### Live View Controls

| Key | Action |
|-----|--------|
| q | Quit |
| : | Enter command mode |
| Tab | Switch camera |
| w/a/s/d | Pan/tilt |
| p | Toggle privacy |
| l | Toggle LED |
| ! | Toggle alarm |
| m | Toggle motion detection |
