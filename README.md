# omarchy-cmd-dictate

Voice-to-text dictation for Hyprland. Press a key to start recording, press again to transcribe and type the result at the cursor position. Uses [whisper.cpp](https://github.com/ggerganov/whisper.cpp) for fast, offline speech recognition with automatic language detection (German, English, etc.).

## Installation

```bash
yay -S omarchy-cmd-dictate
omarchy-cmd-dictate download-model        # downloads base model (~148MB)
```

## Usage

```bash
omarchy-cmd-dictate                       # toggle: start recording / stop + transcribe + type
omarchy-cmd-dictate download-model [SIZE] # download model (tiny|base|small, default: base)
```

Bind to a key in your Hyprland config:

```
bindd = Mod3, D, Voice dictation (toggle), exec, omarchy-cmd-dictate
```

Or source the included config snippet:

```
source = /usr/share/omarchy-cmd-dictate/hyprland-bindings.conf
```

## Dependencies

- [whisper.cpp](https://aur.archlinux.org/packages/whisper.cpp) (provides `whisper-cli`)
- pipewire (provides `pw-record`)
- wtype
- libnotify (provides `notify-send`)

## License

MIT
